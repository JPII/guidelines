java-standards
==========

A summary of Java coding standards. These must be followed for all Java code.

## Coding Standards
* Javadocs are vital and must be used for every public facing method. They must note any possible raised exception, the return result (if any), the method arguments (if any) and a description of the method - this is a minimum, more is better.
* All public facing methods must be input validated and raise exceptions if something is wrong. It's better to catch a bug that may happen than let it grow into something worse.
* No trailing whitespaces. Use sun/oracle coding standards if in doubt.
* Absolutely no already-implemented classes or methods methods. Use interfaces, and have util classes.
* Brackets do not get their own line, unless they are ending a block
* This is only a summary, see http://geosoft.no/development/javastyle.html for a full list
* Alternatively, use http://www.leepoint.net/notes-java/principles_and_practices/style/style-practices-summary.html for a summary

## Purpose
* Clean, readable, reliable code

*To be expanded...*