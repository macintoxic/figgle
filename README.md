```                       
 _____ _         _     
|   __|_|___ ___| |___ 
|   __| | . | . | | -_|
|__|  |_|_  |_  |_|___|
        |___|___|      
```

[![Figgle Build Status](https://ci.appveyor.com/api/projects/status/2vvwieg2ou7pkhst?svg=true)](https://ci.appveyor.com/project/drewnoakes/figgle)
[![Figgle NuGet version](https://img.shields.io/nuget/v/Figgle)](https://www.nuget.org/packages/Figgle/)
[![Figgle Nuget download count](https://img.shields.io/nuget/dt/Figgle)](https://www.nuget.org/packages/Figgle/)

## ASCII banner generation for .NET

```c#
Console.WriteLine(
    FiggleFonts.Standard.Render("Hello, World!"));
```

Produces...

```
  _   _      _ _         __        __         _     _ _
 | | | | ___| | | ___    \ \      / /__  _ __| | __| | |
 | |_| |/ _ \ | |/ _ \    \ \ /\ / / _ \| '__| |/ _` | |
 |  _  |  __/ | | (_) |    \ V  V / (_) | |  | | (_| |_|
 |_| |_|\___|_|_|\___( )    \_/\_/ \___/|_|  |_|\__,_(_)
                     |/
```

The library bundles 265 [FIGlet](http://www.figlet.org/) [fonts](http://www.jave.de/figlet/fonts.html). You can add your own if that's not enough! 

## Installation

Available via [NuGet](https://www.nuget.org/packages/Figgle/):

>Install-Package Figgle

Targets .NET Standard 1.3, so runs pretty much anywhere.

## Other samples

Using `FiggleFonts.Graffiti`:

```
  ___ ___         .__  .__               __      __            .__       .___._.
 /   |   \   ____ |  | |  |   ____      /  \    /  \___________|  |    __| _/| |
/    ~    \_/ __ \|  | |  |  /  _ \     \   \/\/   /  _ \_  __ \  |   / __ | | |
\    Y    /\  ___/|  |_|  |_(  <_> )     \        (  <_> )  | \/  |__/ /_/ |  \|
 \___|_  /  \___  >____/____/\____/  /\   \__/\  / \____/|__|  |____/\____ |  __
       \/       \/                   )/        \/                         \/  \/
```

Using `FiggleFonts.ThreePoint`:

```
|_| _ || _    \    / _  _| _||
| |(/_||(_),   \/\/ (_)| |(_|.
```

Using `FiggleFonts.Ogre`:

```
            _ _          __    __           _     _   _ 
  /\  /\___| | | ___    / / /\ \ \___  _ __| | __| | / \
 / /_/ / _ \ | |/ _ \   \ \/  \/ / _ \| '__| |/ _` |/  /
/ __  /  __/ | | (_) |   \  /\  / (_) | |  | | (_| /\_/ 
\/ /_/ \___|_|_|\___( )   \/  \/ \___/|_|  |_|\__,_\/   
                    |/                                  
```

Using `FiggleFonts.Rectangles`:

```
                                            __ 
 _____     _ _          _ _ _         _   _|  |
|  |  |___| | |___     | | | |___ ___| |_| |  |
|     | -_| | | . |_   | | | | . |  _| | . |__|
|__|__|___|_|_|___| |  |_____|___|_| |_|___|__|
                  |_|                          
```

Using `FiggleFonts.Slant`:

```
    __  __     ____           _       __           __    ____
   / / / /__  / / /___       | |     / /___  _____/ /___/ / /
  / /_/ / _ \/ / / __ \      | | /| / / __ \/ ___/ / __  / / 
 / __  /  __/ / / /_/ /      | |/ |/ / /_/ / /  / / /_/ /_/  
/_/ /_/\___/_/_/\____( )     |__/|__/\____/_/  /_/\__,_(_)   
                     |/                                      
```

## Loading external fonts

Figgle ships with a bunch of fonts (in the `FiggleFonts` class). If you prefer, you can load your own.

Here's an example that loads a font from disk and renders some text with it:

```c#
using var fontStream = System.IO.File.OpenRead("myfont.flf");
var font = FiggleFontParser.Parse(fontStream);
var text = font.Render("Hello World, from My Font");
```
