---
tags:
  - command
---

# /netrun

## Syntax

<!--cmd-syntax-start-->
```eqcommand
/netrun MyProgram
/netrun myprogram "Claw of Qunard" "Ethereal Skyfire" "Shocking Vortex"
```
<!--cmd-syntax-end-->

## Description

<!--cmd-desc-start-->
To run your newly created program, assuming your dll is called MyProgram: `/netrun MyProgram`. The args variable contains whatever parameters you passed when you did the /netrun.
<!--cmd-desc-end-->

You'll first need to bootstrap the .NET runtime, this is easy enough:

```csharp
/plugin mq2dotnetloader
```

This is just a plain old plugin, it loads the .NET runtime, and from the it also loads MQ2DotNet which is where the good stuff happens. To run your newly created program, assuming your dll is called MyProgram:

```csharp
/netrun MyProgram
```

That's it! If all goes according to plan, you should see "Hello <name>" printed in your chat window.

Did I mention you can run as many as you want at the same time?

## See also

- [/netend](cmd-netend.md)
