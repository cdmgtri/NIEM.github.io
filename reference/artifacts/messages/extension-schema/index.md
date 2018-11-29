---
  title: Extension Schema
  icon: fa-plus
  description: Extension schemas define user-created components in an IEPD.  These new components may extend, augment, substitute for, or otherwise reuse components from NIEM - or they may represent completely new content that does not appear in NIEM.
---

{{ page.description }}

{:.note}
> An extension schema must conform to the set of rules defined by the [NDR]({{site.data.links.ndr}}) Extension Schema Document rule set.

The new content that is added in extension schemas is often commonly referred to as "extensions".

<!--more-->

## NIEM JSON and Extension Schemas

In NIEM JSON, it is often easier to define properties and types from different namespaces together in the same JSON schema.  This is because the NIEM conceptual model uses techniques like element substitution and type extension, which do not have direct counterparts in JSON schema.  Because of this, JSON extensions are often added to the same JSON schema that defines the NIEM subset for an IEPD and a separate JSON extension schema is not necessary.

## Conformance Targets

An XML extension schema must declare an ExtensionSchemaDocument conformance target as defined by the [NDR]({{site.data.links.ndr}}).

{:.example}
- 4.0 extension schema document example

```xml
<xs:schema
  ct:conformanceTargets="http://reference.niem.gov/niem/specification/naming-and-design-rules/4.0/#ExtensionSchemaDocument">
<xs:schema>
```
See the page about the [Conformance Target Attribute Specification](../../specifications/conformance-targets/) for more details about how to declare a conformance target attribute and additional possible values.

## EXT Example

```xml
  <?xml version="1.0" encoding="US-ASCII"?>
  <xs:schema targetNamespace="http://release.niem.gov/niem/niem-core/4.0/" version="1" xsi:schemaLocation="http://release.niem.gov/niem/appinfo/4.0/ ../../appinfo/4.0/appinfo.xsd http://release.niem.gov/niem/conformanceTargets/3.0/ ../../conformanceTargets/3.0/conformanceTargets.xsd" ct:conformanceTargets="http://reference.niem.gov/niem/specification/naming-and-design-rules/3.0/#ExtensionSchemaDocument" xmlns:niem-xs="http://release.niem.gov/niem/proxy/xsd/3.0/" xmlns:structures="http://release.niem.gov/niem/structures/3.0/" xmlns:xs="http://www.w3.org/2001/XMLSchema" xmlns:appinfo="http://release.niem.gov/niem/appinfo/3.0/" xmlns:ct="http://release.niem.gov/niem/conformanceTargets/3.0/" xmlns:nc="http://release.niem.gov/niem/niem-core/3.0/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <xs:import schemaLocation="../../proxy/xsd/3.0/xs.xsd" namespace="http://release.niem.gov/niem/proxy/xsd/3.0/"/>
    <xs:import schemaLocation="../../structures/3.0/structures.xsd" namespace="http://release.niem.gov/niem/structures/3.0/"/>
    <xs:element name="DateRepresentation" abstract="true"/>
    <xs:element name="DateTime" type="niem-xs:dateTime" substitutionGroup="nc:DateRepresentation"/>
  </xs:schema>
```
