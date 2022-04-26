---
title: "Obfuscator configurations"
description: "The configurations and versions of obfuscators we evaluated."
lead: "The configurations and versions of obfuscators we evaluated."
date: 2022-04-17T13:59:39+01:00
lastmod: 2022-04-17T13:59:39+01:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 130
toc: true
---

## VMProtect v3.5


| Protection Options       |            |                       | The simplest configuration we recommend | The most critical configuration we can handle  |   |   |   |   |   |
|--------------------------|------------|-----------------------|-----------------------------------------|------------------------------------------------|---|---|---|---|---|
| Functions for Protection | Protection | Compilation Type      | Virtualization                          | Ultra (Virtualization+Mutation)                |   |   |   |   |   |
|                          |            | Lock To Serial Number | No                                      | No                                             |   |   |   |   |   |
| Options                  | File       | Memory Protection     | No                                      | Yes                                            |   |   |   |   |   |
|                          |            | Import Protection     | No                                      | Yes                                            |   |   |   |   |   |
|                          |            | Resource Protection   | No                                      | Yes                                            |   |   |   |   |   |
|                          |            | Pack the Output File  | No                                      | Yes                                            |   |   |   |   |   |
|                          | Detection  | Debugger              | No                                      | No                                             |   |   |   |   |   |
|                          |            | Virtualization Tools  | No                                      | Yes                                            |   |   |   |   |   |
|                          | Additional | VM Segments           | .vmp                                    | .vmp                                           |   |   |   |   |   |

> Settings in "Additional" options have no influence on execution, so they are irrelevant to our experiment.										

## VMProtect v2.13.8
| Protection Options        |                  |                      | The simplest configuration we recommend | The most critical configuration we can handle |
|---------------------------|------------------|----------------------|-----------------------------------------|-----------------------------------------------|
| Procedures for protection | Compilation Type |                      | Virtualization                          | Ultra (Virtualization+Mutation)               |
| Options                   | Level            |                      | Maximum protection                      | Maximum protection                            |
|                           | Detection        | Debugger             | No                                      | No                                            |
|                           |                  | Virtualization tools | No                                      | Yes                                           |
|                           | Compilation      | Virtual machines     | 1                                       | 1   

## Code Virtualizer v2.2.2

| Extra Options               | The simplest configuration we recommend | The most critical configuration we can handle |
|-----------------------------|-----------------------------------------|-----------------------------------------------|
| Location of Protection Code | Insert in last section                  | Insert in last section                        |
| Virtualize Strings          | Disable                                 | Ansi/Unicode/Ansi+Unicode Strings             |
| Compress Virtual Machine    | No                                      | Yes                                           |
| Strip Relocations           | No                                      | Yes                                           |
| Fake Stack Emulation        | No                                      | Yes                                           |



> "Location of Protection Code" and "Strip Relocations" have no influence on execution. Program for knowledge leaking has no strings. So "Virtualize Strings" and the former two settings are irrelevant.										
										

## Code Virtualizer v3.0.7
| Options                  |                              | The simplest configuration we recommend | The most critical configuration we can handle |
|--------------------------|------------------------------|-----------------------------------------|-----------------------------------------------|
| Protection Options       | Location of Protection Code  | Insert in new Section                   | Insert in new Section                         |
|                          | Encrypt Strings in VM macros | None                                    | ANSI Strings, Unicode Strings                 |
|                          | Compress Virtual Machine     | Disable                                 | Enable                                        |
| Extra Protection Options | Entry Point Virtualization   | No                                      | Yes                                           |
|                          | Strip Relocations            | No                                      | Yes                                           |
|                          | Optimize for Windows on ARM  | No                                      | No                                            |


> We do experiment on Intel x86 instructions, so "Optimize for Windows on ARM" is not cosidered. Advanced options are irrelevant to the experiment, since they have no effect on the knowledge leaking process.										
										
## Themida v2.2.2

| Options            |                           | The simplest configuration we recommend | The most critical configuration we can handle |
|--------------------|---------------------------|-----------------------------------------|-----------------------------------------------|
| Protection Options | Anti-Debugger Detection   | Disable                                 | Disable                                       |
|                    | Advanced API-Wrapping     | Disable                                 | Level 2                                       |
|                    | Compress                  | None                                    | Application, Resources, SecureEngine          |
|                    | Anti Dumpers              | No                                      | Yes                                           |
|                    | Anti-Patching             | No                                      | Yes                                           |
|                    | Entry Point Obfuscation   | No                                      | Yes                                           |
|                    | Metamorph Security        | No                                      | Yes                                           |
|                    | Monitor Blockers          | No                                      | Yes                                           |
|                    | Resources Encryption      | No                                      | Yes                                           |
|                    | Memory Guard              | No                                      | Yes                                           |
|                    | Dephi/BCB Form Protection | No                                      | Yes                                           |
|                    | VMWare/Virtual PC         | Yes                                     | Yes                                           |
|                    | When Debugger Found       | Display Message                         | Display Message                               |
| Advanced Options   | Hide from PE scanner      | Standard                                | Standard                                      |


> Other options in advanced options are irrelevant to the experiment, since programs for knowledge leaking do not need extra dll files, .NET assemblies, manifest files and splash images.										
										

## Themida v3.0.7

| Options                  |                                         | The simplest configuration we recommend | The most critical configuration we can handle |
|--------------------------|-----------------------------------------|-----------------------------------------|-----------------------------------------------|
| Protection Options       | Anti-Debugger Detection                 | Disable                                 | Disable                                       |
|                          | Advanced API-Wrapping                   | Disable                                 | Enable                                        |
|                          | Compress and Encrypt                    | None                                    | Application, Resources, SecureEngine          |
|                          | Encrypt Strings in VM macros            | None                                    | ANSI Strings, Unicode Strings                 |
| Extra Protection Options | Detect File/Registry Monitors           | No                                      | Yes                                           |
|                          | Entry Point Virtualization              | No                                      | Yes                                           |
|                          | Anti-File patching                      | No                                      | Yes                                           |
|                          | Anti-Sandbox                            | No                                      | Yes                                           |
|                          | Perform Protection checks on VM macros  | No                                      | Yes                                           |
|                          | Allow execution under VMware/Virtual PC | Yes                                     | Yes                                           |

>Extra and advanced options are irrelevant to the experiment, since our programs for knowledge leaking have nothing to do with network interaction and extra dll/data loading(XBundle). Splash image, manifest file and antivirus certificate are also unneeded.									
										

## Obsidium v1.6.7

| Options           |                                                              | The simplest configuration we recommend | The most critical configuration we can handle |
|-------------------|--------------------------------------------------------------|-----------------------------------------|-----------------------------------------------|
| Basic settings    | Encrypt  resources                                           | No                                      | Yes                                           |
|                   | Remove exports                                               | No                                      | Yes                                           |
|                   | Compression                                                  | No                                      | Yes                                           |
|                   | Alternate compression method                                 | No                                      | Yes                                           |
|                   | Debugger checks                                              | No                                      | No                                            |
|                   | Application password:                                        | No                                      | No                                            |
|                   | Set environment variables                                    | No                                      | No                                            |
| Advanced settings | Keep overlays                                                | No                                      | Yes                                           |
|                   | Control overlay access                                       | No                                      | Yes                                           |
|                   | Encrypt overlays                                             | No                                      | Yes                                           |
|                   | Alternate control method                                     | No                                      | Yes                                           |
|                   | Alternate control method 2                                   | No                                      | Yes                                           |
|                   | Visual Studio fix                                            | No                                      | Yes                                           |
|                   | Void unneeded resources                                      | No                                      | Yes                                           |
|                   | Delphi/BCB obfuscation                                       | No                                      | Yes                                           |
|                   | Remove bytes at OEP                                          | No                                      | Yes                                           |
|                   | Disallow execution in virtual machines                       | No                                      | No                                            |
|                   | Delphi/BCB 3rd-party compatibility                           | No                                      | Yes                                           |
|                   | Legacy import protection                                     | No                                      | Yes                                           |
|                   | Runtime patching                                             | No                                      | Yes                                           |
|                   | Runtime tracing                                              | Yes                                     | Yes                                           |
|                   | Check encrypted sections                                     | No                                      | No                                            |
|                   | Don't display any messages                                   | No                                      | Yes                                           |
|                   | Disable API emulation                                        | No                                      | Yes                                           |
|                   | Dynamic protection API access                                | No                                      | Yes                                           |
|                   | Keep import data                                             | No                                      | Yes                                           |
|                   | Let windows load DLLs                                        | No                                      | Yes                                           |
|                   | Verify file size                                             | No                                      | Yes                                           |
|                   | Random section names                                         | No                                      | Yes                                           |
|                   | Limit number of instances                                    | No                                      | No                                            |
|                   | Don't hook DLLs                                              | No                                      | Yes                                           |
|                   | lLicense expiration system clock checkPreserve PDB signature | No                                      | Yes                                           |
|                   | lLicense expiration system clock checkPreserve PDB signature | No                                      | Yes                                           |
