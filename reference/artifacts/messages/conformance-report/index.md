---
title: Conformance Report
description: A conformance report specifies how and to what degree the IEPD is NIEM-conformant.
icon: fa-check
---

{{ page.description }}

## ConTesA Report

The [Conformance Testing Assistance (ConTesA)]({{ site.data.pages.contesa }}) checks uploaded schemas against Schematron rules from the [Naming and Design Rules (NDR)]({{ site.data.pages.ndr }}).

{:.example}
- The images below show portions of the spreadsheet version of the conformance report generated by `ConTesA`.
- This first image shows the summary - how many rules were run, how many rules passed, and how many rules failed.

![ConTesA summary example](assets/contesa-summary.png)

{:.example}
- This image shows the NDR rules that failed and the schema line numbers where it occurred.

![ConTesA rule failures example](assets/contesa-failed.png)

## Additional validation steps

Additional information can also be included specifying any additional steps that were taken to manually review and validate rules that are not automated, like free-text rules from the [Naming and Design Rules (NDR)]({{ site.data.pages.ndr }}) and the [Model Package Description (MPD) Specification]({{ site.data.pages.mpd }}).  See the [MPD Specification, Appendix D. Conformance Assertion Example]({{ site.data.links.mpd_spec}}#appendix_D) for more on what this might look like.