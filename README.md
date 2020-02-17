# HaTeXML

A syntax inspired by the TeX typesetting language developed by Donald Knuth for generating HTML from templates.

# What is it for?

Tentatively, it will just translate tags from it's own syntax into HTML.

Thus:

```
\p{
    Please reference \i{item 11} on the \a(href=http://ref.to/rules.html){list of rules} for clarification.
}
```

Translates to:

```
<P>Please reference <I>item 11</I> on the <A HREF+"http://ref.to/rules.html">list of rules</A> for clarification.</P>
```

Further, the HaTeXML syntax provides a few added benefits such as macros which can be expressed inline anywhere in the document or included from external files. These macros are referenced as normal tags as such:

```
\def[tablerow]{\tr{\td{$1}\td{$2}}}
\tablerow["Last Name", "First Name"]
```

This opens up interesting possibilities of libraries of templates, object classes and dynamic HTML generation within templates.

# Why the name HaTeXML

HaTeXML is not about hating HTML or XML. In fact, HTML is a wonderful syntax and it's a wonderful thing that it was the chosen standard for the web, just like how great and wonderful it is that JavaScript would be created in 2 weeks as a web standard instead of Lisp.
