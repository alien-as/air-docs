<h1>App. Descriptor</h1>

* [Template](#template)
* [Schema](#schema)
  * [Locale Strings](#locale-strings)
  * [Identity](#identity)
  * [Initial Window](#initial-window)
  * [Platform Specifics](#platform-specifics)

# Template

Every AIR application has a descriptor,
which follows this common template:

```xml
<?xml version="1.0" encoding="utf-8"?>
<application xmlns="http://ns.adobe.com/air/application/AIR_VER">
    <filename>sample</filename>
    <name>Sample</name>
    <id>vendor.sample</id> 
    <versionNumber>0.1.0</versionNumber> 
    <copyright>Copyright © 2090 Vendor</copyright> 

    <initialWindow> 
        <title>Sample</title> 
        <visible>true</visible>
        <content>sample.swf</content>
    </initialWindow>
</application>
```

Note:

* `AIR_VER` must be a AIR version supported by the host SDK.

# Schema

## Locale Strings

Multiple `<text/>` elements are allowed under some
contexts; for example, under application's `<description/>`:

```xml
<application>
    <description> 
        <text xml:lang="en">This is an example.</text>
        <text xml:lang="fr">C'est un exemple.</text>
        <text xml:lang="es">Esto es un ejemplo.</text>
    </description>
</application>
```

The `xml:lang` attribute is a language code (as per [RFC-4646](https://www.ietf.org/rfc/rfc4646.txt)).

## Identity

_Under `<application/>`..._

#### \<filename>filename\</filename>

`<filename/>` represents installation folder name or executable name.

* **Constraint pattern:** `(?x) [  \x00-\x1F \*  \"  \:v \>  \<  \?  \\  \|  ]`. No trailling dot allowed.

#### \<name>Conventional Name\</name>

`<name/>` accepts [locale strings](#locale-strings).

#### \<id>vendor.app\</id>

* **Required.**

* **Constraint pattern:** `(?x) [ A-Z a-z 0-9 . \- ]`.

#### \<el>XXX\</el>


#### \<el>XXX\</el>


#### \<el>XXX\</el>


#### \<el>XXX\</el>


#### \<el>XXX\</el>


#### \<el>XXX\</el>


#### \<el>XXX\</el>



## Initial Window



## Platform Specifics