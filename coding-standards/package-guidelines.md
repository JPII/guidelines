package-guidelines
==========

A summary of packages and their usage.

## Purpose
* To organize classes into definable sections
* To separate self-reliant classes (such as an util package)

## Structure
* **Namespace:** com.jpii.projectname.packagename.subpackagename
* Note that third party code may have a different namespace

## General guidelines
* Avoid having a single class in a package (exceptions include the root package with the main class)
* Keep package names lower-case with short (yet memorable) identifiers
* Third party code should be added as it was provided, if possible
