# MeshWidgetExample

## Requirements
- Unreal Editor 5.3.2
- Visual Studio 2022
- MSVC v143 - VS 2022 C++ x64/x86 build tools (v14.38-17.8) (Out of support)
- .NET 6.0 Runtime (Out of support)

### Maybe manually select MSVC version for UnrealBuildTool(UBT)
***UBT may not happy when you have multi MSVC version in VS2022, cuz it default use higher version to compile.***

- Open **%APPDATA%/Unreal Engine/UnrealBuildTool/BuildConfiguration.xml** and modify kind of
```xml
<?xml version="1.0" encoding="utf-8"?>
<Configuration xmlns="https://www.unrealengine.com/BuildConfiguration">
    <WindowsPlatform>
        <!-- Please Replace Your MSVC version !! -->
        <!-- Check Your MSVC version: "C:\Program Files\Microsoft Visual Studio\2022\Community\VC\Tools\MSVC" !!-->
        <CompilerVersion>14.38.33130</CompilerVersion>
    </WindowsPlatform>
</Configuration>
```

## Building
- Run `gen_vs2022.bat`
- Open `MeshWidgetExample.sln` and Compile/Run

## References
- https://dev.epicgames.com/documentation/unreal-engine/API/Runtime/UMG/SMeshWidget
- https://youtu.be/OyY3OYbNK7s?t=863
- https://forums.unrealengine.com/t/smeshwidget-hardware-instanced-slate-meshes-thread/58020/
- https://forums.unrealengine.com/t/nick-darnell-loading-screen-plugin-great-but-i-have-some-questions/67304
- https://www.youtube.com/watch?v=pUp7QVPaZHI