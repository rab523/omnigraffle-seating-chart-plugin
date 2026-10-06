# Update Seats from Roster for OmniGraffle

Paste an instrument roster to update names in an existing color-coded seating chart. The plug-in can duplicate existing seats when a section needs more places.

**This is a layout-specific tool, not a blank-canvas chart generator.** Start with a copy of a chart containing colored seat shapes, with at least one template seat for each instrument section. No real student list or school seating chart is included.

## Install and use

1. Download [UpdateSeatsFromRoster-Shared.omnijs](UpdateSeatsFromRoster-Shared.omnijs?raw=true) and open it with OmniGraffle. Follow the plug-in installation prompt; your edition must support Omni Automation.
2. Make a working copy of your chart and select its canvas.
3. Copy a roster formatted like [sample-roster.txt](sample-roster.txt), then choose **Update Seats from Roster - Shared** in the Automation menu.
4. Review the pasted roster and choose **Update**. Inspect the resulting positions and the completion report before sharing the chart.

Use section headings such as `Flute`, `Bass Clarinet`, `Alto Saxophone`, `Trumpet`, or `Percussion`, followed by one `Last, First` entry per line. Only the first word of the given name is used. Use `Saxophone` in saxophone headings.

## Layout requirements

Seat text must contain at least three characters. Numeric labels and certain equipment labels are excluded. Match the RGB values below (each channel ranges from 0 to 1); edit `SECTION_COLORS` if your chart uses different colors.

| Section | R | G | B |
|---|---:|---:|---:|
| Flute | .80 | .80 | .80 |
| Oboe | 0 | 1 | 1 |
| Clarinet | .60 | .60 | .60 |
| Bass Clarinet | .40 | .40 | .40 |
| Bassoon | .50 | .56 | .73 |
| Alto Saxophone | .96 | .74 | 0 |
| Tenor Saxophone | .87 | .68 | .15 |
| Baritone Saxophone | 1 | 0 | 0 |
| Trumpet | .84 | .68 | .64 |
| Horn | 1 | .75 | .75 |
| Trombone | 1 | .47 | 0 |
| Euphonium | 1 | 1 | .25 |
| Tuba | .41 | .74 | .21 |
| Percussion | 1 | 1 | 1 |

White, black, or unfilled percussion candidates must be near the top of the canvas (y below 130). Instrument rows use a 30-point tolerance. Most sections fill rows from bottom to top, right to left; percussion uses top to bottom, left to right. These assumptions may require adapting the code to your chart.

Surplus seats are reported, not automatically erased; old names may remain in unused seats. Review and remove those locally. A section without a matching seat template cannot be generated automatically.

## Privacy and validation

The plug-in reads the clipboard to prefill its roster form and edits the current document locally. It has no network upload functionality. Keep real rosters and completed charts out of this public repository. The sample uses fictional names.

The shared copy has a separate identifier to preserve an installed personal copy. JavaScript syntax and roster parsing were checked; a fresh OmniGraffle layout test of this shared copy remains pending.
