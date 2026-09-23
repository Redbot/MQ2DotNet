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
To run your newly created program, assuming your dll is called MyProgram: `/netrun MyProgram`. That's it! If all goes according to plan, you should see "Hello &lt;name&gt;" printed in your chat window.
<!--cmd-desc-end-->

To run it, put your compiled dll, along with the two attached ones, in your Release directory. You'll first need to bootstrap the .NET runtime, this is easy enough:

```csharp
/plugin mq2dotnetloader
```

This is just a plain old plugin, it loads the .NET runtime, and from the it also loads MQ2DotNet which is where the good stuff happens. To run your newly created program, assuming your dll is called MyProgram:

```csharp
/netrun MyProgram
```


That's it! If all goes according to plan, you should see "Hello &lt;name&gt;" printed in your chat window.

The args variable contains whatever parameters you passed when you did the /netrun, and you don't even have to use "this GetArg shit":

```csharp
	public static async Task Main(string[] args)
	{
		foreach (string arg in args)
			MQ2.WriteChat($"Hello {arg}");
	}
```

This would cast each spell in sequence, e.g.

```csharp
/netrun myprogram "Claw of Qunard" "Ethereal Skyfire" "Shocking Vortex"
```

## See also

- [/netend](cmd-netend.md)
