---
  title: Artifacts
  icon: fa-sitemap
  description: Learn about the kinds of files that make up NIEM releases and IEPDs.
  links:
  - url: /reference/artifacts/overview/
  - url: /reference/iepd/
    group: iepd
  - url: /reference/artifacts/iep/
    group: iepd
  - url: /reference/artifacts/subset-schema/
    group: iepd
  - url: /reference/artifacts/extension-schema/
    group: iepd
  - url: /reference/artifacts/xml-catalog/
    group: other
  - url: /reference/artifacts/code-lists/
    group: niem
  todo:
  - move over release artifacts
  - move over releases
  - move over core-supplement
  - add mpd catalog
  - add domain update
---

See a [one-page overview](overview) for excerpts of each of the major artifacts. You may also choose an item on this page for which you need more information

## Conformant Artifacts

NIEM Conformant Artifacts are the substantive components created to represent the NIEM or NIEM exchange data model. Typically they are packaged into several collections of text, JSON, XML, and binary files.

{:.note}
>
> An artifact is a NIEM-conformant artifact if and only if it
>
>- has a Conformance Target defined within a NIEM specification,
>- adheres to all normative rules applicable to its Conformance Target, and
>- references the namespaces of any NIEM components used within its definition.

<!--
Main Specifications
- Conformance (internal organization link)
- Conformance Targets Attribute (internal organization link)
- HLVA (internal organization link)
- MPD (internal organization link)
- NDR (internal organization link)
- Schematron in XML (internal organization link)

Artifact Specifications
- Code List
- Extension Schema
- Subset Schema
- Schema Document Set
-->

### Special Artifacts

{% assign advancedLinks = page.links | where: "group", "special" %}
{% include icon-list.html links=advancedLinks %}

### NIEM IEPD-Specific Artifacts

{% assign iepd = page.links | where: "group", "iepd" %}
{% include icon-list.html links=iepd %}

### Other NIEM-Specific Artifacts

{% assign niem = page.links | where: "group", "niem" %}
{% include icon-list.html links=niem %}

## Other Artifacts

{% assign other = page.links | where: "group", "other" %}
{% include icon-list.html links=other %}
