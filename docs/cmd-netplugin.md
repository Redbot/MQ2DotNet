---
tags:
  - command
---

# /netplugin

## Syntax

<!--cmd-syntax-start-->
```eqcommand
/netplugin myplugin
/netplugin myplugin noauto
/netplugin myplugin unload
/netplugin myplugin unload noauto
```
<!--cmd-syntax-end-->

## Description

<!--cmd-desc-start-->
Copy the resulting dll to your Release folder, and load/unload with `/netplugin myplugin`. Just like you would for a normal plugin. The list of plugins to be loaded automatically is stored in MQ2DotNet.ini.
<!--cmd-desc-end-->

Copy the resulting dll to your Release folder, and load/unload with:

```csharp
/netplugin myplugin
/netplugin myplugin noauto
/netplugin myplugin unload
/netplugin myplugin unload noauto
```


Just like you would for a normal plugin. The list of plugins to be loaded automatically is stored in MQ2DotNet.ini.
