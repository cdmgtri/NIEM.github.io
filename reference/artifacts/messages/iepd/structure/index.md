---
  title: IEPD Structure
  short: Structure
  icon: fa-sitemap
  description: IEPD Structure
---

Information Exchange Package Documentation (IEPD) is a set of NIEM artifacts whose principal content is schema documents, the purpose for which is to define and declare reusable data components for information exchanges or to define the exchanges themselves. They are a NIEM artifact defined by the Model Package
Description Specification (MPD-Spec) and are a kind of Model Package Description (MPD).

## IEPD Artifacts

For well-formed IEPDs, several common artifacts are found contained in their definitions:

- A `README` artifact
- MPD Catalog describing the contents of the IEPD
- Subset, Extension, or External Schema Documents which define a self-consistent Schema Document Set (SET)
- At least one declared IEP conformance target
- Sample instance documents that validate to the SET
- A Change Log describing incremental changes and updates to the IEPD
- A Conformance Report specifying how and to what degree the IEPD is NIEM-Conformant

### The `README` Artifact

A `README` artifact (formerly known as a master document) is mandatory for all IEPDs. IEPDs are often built by different developers, and may be registered into a repository for reuse by many other users, developers, and implementers; therefore, a minimal form of documentation is absolutely necessary. An IEPD `README` file is the primary source and starting point for human readable documentation, and should reference (and describe) any other separate documentation artifacts. This requirement ensures that baseline documentation is consistently rooted in a clearly visible artifact within each IEPD.
