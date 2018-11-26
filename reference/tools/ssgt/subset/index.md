---
  title: Subset
  icon: fa-filter
  list:
  - url: /reference/tools/ssgt/subset/add/
  - url: /reference/tools/ssgt/subset/remove/
  - url: /reference/tools/ssgt/subset/generate/
---

The SSGT allows you to pick and choose specific parts of a release to include in a subset.  This subset, which will likely have many fewer files and components than the full release, can be used in your IEPD.  While you can reuse a full release package, it is easier to understand and work with only the schemas and the components that you need.

If you are developing multiple IEPDs, you can build a custom subset for each one or one larger subset that supports the requirements from each IEPD.

{:.note}
- This tool does not have user accounts.
- To **[save your work](generate)**, you must download either the individual **wantlist** file (a SSGT-generated XML file that stores your selections) or the **full subset zip file**, which will contain the latest wantlist.
- The **[only way to resume your work](../options/resume-work)** later on is to upload your latest wantlist file.

Please see **[Subset Schemas]({{ site.data.pages.subset }})** for more information about what a subset is.

## Cardinality constraints

Subsets also let you constrain how many times an element may appear nested within a type.  As a reference model, NIEM usually sets cardinality to optional and over-inclusive (`minOccurs="0" maxOccurs="unbounded"`) to support a wide variety of requirements.

In an exchange, you can customize the cardinality to your exact requirements.  Make elements required, limit occurrences to only once, or set any other cardinality as long as it does not conflict with the original cardinality from NIEM (an element that is required in NIEM cannot be made optional in a subset).

The subset example above shows updated cardinality, setting the given name and surname to occur exactly once and setting middle name to be optional with multiples allowed.

## Dependencies

The SSGT will automatically calculate all required dependencies whenever a component is added to the subset list.

- User-selected components will appear in bold font in the subset panel.
- Dependencies will appear in regular font.

If you later remove a selected component, dependencies that are no longer necessary will also be removed.
