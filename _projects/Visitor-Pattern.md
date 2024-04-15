---
layout: page
title: Visitor Design Pattern 
description: group project, class lecture, and examples about the visitor pattern
img: assets/img/visitor.png
importance: 2
category:  coursework
---

*A short writeup about the visitor pattern, housing resources used in-class as well as some additional notes*

## Lecture Slides

[Visitor Pattern, 15 April 2024]({{site.baseurl}}/assets/pdf/visitorpatternlect.pdf)

## Code Example

[Geometry Program Example]({{site.baseurl}}/assets/code/visitor-code-zip.zip)

## Abridged Notes

The Visitor is a **behavioral** design pattern that allows for separation of methods from a collection of objects at different levels in an inheritance heirarchy. The GoF book mentions a "heterogenous collection" of objects.

**Behavioral** patterns focus on how different classes and groups interact (or *behave* 😉), while **Structural** patterns focus on how classes and objects are composed, through is-a, has-a, interfaces, etc. Essentially, the pattern is focused on how something is *structured*. 

Consider writing a program that deals with different types of files. We want to save these files somehow, but I will argue that "saving" a file is not a method of a `.PDF`, `.MOV`, `.TXT` object. It somewhat violates the single responsibility principle to have a file know how to save itself in the context of a larger system. 

```java
class PDFFile {
    void save() {}
}

class TXTFile {
    void save() {}
}

class MOVFile {
    void save() {}
}
```

Instead of having a `<fileType>.save()` method in every implementation, we instead separate all save methods to a separate actor:

```java
class FileSaver {
    void save(PDFFile f) {}
    void save(TXTFile f) {}
    void save(MOVFile f) {}
}
```

Since these file types represent differnt underlying formats, how we save them may be different, so a separate method is needed for each.

However, due to restrictions of most programming languages, we cannot simple use `FileSaver` as a utility class to save files, due to **single dispatch**. In analogy, we cannot just start from the FileSaver, feed it arbitrary files, and have it save all of them correctly.

Instead, `FileSaver` must **visit** each of the files first, such that they can then `<fileType>.accept(visitor)`. This is a workaround that allows for **double dispatch** to be used under the hood. Hand waving the compiler specifics, this seemingly additional step allows for us to get runtime benefits without messy type casting.
