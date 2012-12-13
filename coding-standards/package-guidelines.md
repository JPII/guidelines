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

**From http://efsavage.com/blog/posts/java_package_conventions/**
* Names should be all lowercase. Uppercase and mixed case denote other concepts in Java and there’s no need to muddy the waters further.
* Names should be alphanumeric, preferably just alphabetical.
* Do not use version numbers or dates (see below for a possible exception).
* Use tld.domain-you-own.project/library.* for distributed or published code. This follows with Sun’s convention, and is the only way to know a name is globally unique, or at least that you are the one that’s allowed to use it.
* Do not use tld.domain-you-own.* for internal code that should not be distributed. I typically just use the project or library’s name as the first segment. This convention can be useful in signaling other developers that code is for internal use only, and if something is converted from internal to external usage, this will help identify which version an application was built against.
* Package names that are nouns should be singular (mycompany.myproject.account). This maintains consistency with packages that are named for actions (mycompany.myproject.search) and adjectives (mycompany.myproject.common).
* Store DAOs in a “data” subpackage. This helps the tree-views in IDEs and also allows for easier control of logging. If you’re being formal and encapsulate DAO operations in a manager class, the manager class should not be in the data package because it’s grammar is business-based, not persistence-based.
* Classes that are heavily dependent on third-party packages should be in a subpackage named for the primary dependency. A Hibernate implementation of your DAO should live in mycompany.myproject.data.hibernate. This helps greatly with logging configuration. This is one place where version numbers are permissible, such as mycompany.myproject.data.hibernate3. Use this exception very sparingly, as it can be confusing with regards to forward compatibility.
* Classes that are extensions of third-party code should be named for the dependency and be outside of the project’s or product’s context. For example, if you are creating a new type of controller for Spring MVC that does not depend on project-specific code, put it in mycompany.spring.controller. If it is integrated with the application, see the previous point.
*Don’t expose organizational details in the package structure (mycompany.mydepartment.myproject). Naming packages by department, office, or region will surely be confusing soon due to management’s penchant to reorganize and reassign.
