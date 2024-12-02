# NoRSAT

## Synopsis

A PowerShell module to manage Active Directory without the Remote Server Administration Tools.

## Description

The goal of this project is to write functions that can replace the most commonly used cmdlets in the **ActiveDirectory**  PowerShell module.

### Design Principles

- All code must be open source
- Structure and portability:
  - Avoid code re-use by functions in the module
  - Also provide a way for individual functions to be pulled and work independently (map any function dependencies and export individual function "packages")
- Methods:
  - Use .NET types whenever possible
  - Use the ADSISearcher type if necessary
  - Use embedded C# code?
- Focus on 'Get' functions over 'Set' functions
- Function prefix 'NR': `{Verb}-NR{Noun}`
- Return native Active Directory object types that are consistent with the types returned by the related ActiveDirectory module's cmdlets; return rich custom objects otherwise
