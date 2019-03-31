<h1>App. Descriptor</h1>

> **Note:**
> Still incomplete. For now prefer:
>
> * [AIR application descriptor files](https://help.adobe.com/en_US/air/build/WS5b3ccc516d4fbf351e63e3d118666ade46-7ff1.html)
> * [The application descriptor file structure](https://help.adobe.com/en_US/air/build/WS5b3ccc516d4fbf351e63e3d118666ade46-7f84.html)
> * [AIR application descriptor elements](https://help.adobe.com/en_US/air/build/WSfffb011ac560372f2fea1812938a6e463-8000.html)

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

#### \<versionNumber/> and \<versionLabel/>




#### \<el>XXX\</el>


#### \<el>XXX\</el>


#### \<el>XXX\</el>


#### \<el>XXX\</el>


#### \<el>XXX\</el>


#### \<el>XXX\</el>



## Initial Window



## Platform Specifics