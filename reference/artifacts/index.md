---
  title: Artifacts
  icon: fa-sitemap
  description: Learn about the kinds of files that make up NIEM releases and IEPDs.
  links:
  - url: /reference/iepd/
    group: iepd
  - url: /reference/artifacts/iep/
    group: iepd
  - url: /reference/artifacts/subset-schema/
    group: iepd
  - url: /reference/artifacts/extension-schema/
    group: iepd
  - url: /reference/artifacts/core-supplement/
    group: niem
  - url: /reference/artifacts/code-lists/
    group: niem
  - url: /reference/artifacts/xml-catalog/
    group: other
  todo:
  - move over release artifacts
  - move over releases
  - move over core-supplement
  - add mpd catalog
  - add domain update
---

NIEM artifacts are the files that represent NIEM releases or a NIEM information exchange data model. Typically they are packaged into several collections of text, JSON, XML, and binary files.

<<<<<<< HEAD
### IEPD-Specific Artifacts

These artifacts relate to

{% assign iepd = page.links | where: "group", "iepd" %}
{% include icon-list.html links=iepd %}
=======
## Release Artifacts

Some of the artifacts below are specific to NIEM releases; others show how NIEM releases implement common kinds of artifacts like documentation spreadsheets and change logs.

Click on the `Release Artifacts...` section in the sidebar for more or jump directly to a NIEM release artifact below:

{% assign releasesPage = site.pages
    | where: "url", "/reference/artifacts/releases/" | first %}
{% include icon-list.html links=releasesPage.links %}

## IEPD Artifacts

These artifacts are specific to NIEM messages.

Click on the `IEPD Artifacts...` section in the sidebar for more or jump directly to an IEPD artifact below:

{% assign messagesPage = site.pages
    | where: "url", "/reference/artifacts/messages/" | first %}
{% include icon-list.html links=messagesPage.links %}
>>>>>>> 43c9767... rel

### General NIEM Artifacts

{% assign niem = page.links | where: "group", "niem" %}
{% include icon-list.html links=niem %}

## General Artifacts

{% assign other = page.links | where: "group", "other" %}
{% include icon-list.html links=other %}
