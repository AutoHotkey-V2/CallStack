# CallStack [![AutoHotkey2](https://img.shields.io/badge/Language-AutoHotkey2-red.svg)](https://autohotkey.com/)

This library uses [AutoHotkey Version 2](https://autohotkey.com/v2/). (Tested with [AHK v2.0-a100-52515e2 x64 Unicode](https://autohotkey.com/boards/viewtopic.php?p=242306#p242306)) 

## Usage 

Include `CallStack.ahk` from the `lib` folder into your project using standard AutoHotkey-include methods.

```autohotkey
#include <CallStack.ahk>

foo()
return

foo(){
	cs := CallStack()
	# Print the current callstack
	for level, obj in  CallStack() { 
		if (A_Index > 1 )
			str := str . " => "
		str := str . obj.function	
	}
	MsgBox str
}
```

For usage examples have a look at the files in the *examples* folder.

For more detailed documentation have a look into the source file *lib\CallStack.ahk*