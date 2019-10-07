# NetCoreBeauty

## What is it?
Move a .NET Core app runtime components and dependencies into a sub-directory and make it beauty.

## Before Beauty
![before_beauty](before_beauty.png)

## After Beauty
![after_beauty](after_beauty.png)

## How to use?
1. Add Nuget reference into your .NET Core project.
```
dotnet add package nulastudio.NetCoreBeauty
```
your `*.csproj` should be similar like this
```
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp2.1</TargetFramework>
    <!-- beauty into sub-directory, default is libs, quote with "" if contains space  -->
    <BeautyLibsDir>libraries</BeautyLibsDir>
    <!-- set to True if you want to disable -->
    <DisableBeauty>False</DisableBeauty>
    <!-- <BeautyAfterTasks></BeautyAfterTasks> -->
    <!-- set to True if you want to disable -->
    <DisablePatch>False</DisablePatch>
    <!-- set to a repo mirror if you have troble in connecting github -->
    <PatchCDN>https://github-like.com/someone/HostFXRPatcherMirror</PatchCDN>
  </PropertyGroup>

  <ItemGroup>
    <PackageReference Include="nulastudio.NetCoreBeauty" Version="1.0.4" />
  </ItemGroup>

</Project>
```
when you run `dotnet publish` , everything is done automatically.

2. Use the binary application if your project has already be published.
```
Usage:
ncbeauty <beautyDir> [<LibsDir>]
```
for example
```
ncbeauty /path/to/publishDir
```

## Mirror
if you have troble in connecting github, use this mirror
```
https://gitee.com/liesauer/HostFXRPatcher
```
