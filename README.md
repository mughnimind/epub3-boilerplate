# epub3-boilerplate ebook template

[EPUB version 3.2](https://www.w3.org/publishing/epub32/epub-spec.html) template with simplistic, yet universal `css` stylesheet.

## Usage

In order to build this ebook [`7za`](https://www.7-zip.org/download.html) must be installed. To generate also `mobi` format, install [KindleGen](https://www.amazon.com/gp/feature.html?ie=UTF8&docId=1000765211).

PowerShell:

```
$ ./build.ps1
```

The output are two files: `template.epub` and `template.mobi` for Kindle.

## Bonus: reading time

Nice feature is to have a reading time hint. This can be calculated as number of words divided by an averange reading speed (250 words per minute for an adult). To get the number of words use my PHP script:

```
$ php ./count-words.php "./template/Content/ch0?.xhtml"
```

Use it as `<meta property="schema:wordCount">xxx</meta>` metadata field.

## Validation

[`epubcheck`](https://github.com/w3c/epubcheck)
```
Validating using EPUB version 3.2 rules.
No errors or warnings detected.
```

## Common sections (epub:type):
 - frontmatter: titlepage, halftitlepage, seriespage, acknowledgments, contributors, dedication
 - bodymatter: foreword, abstract, preface, preamble, introduction, epigraph, prologue, part, chapter, footnote(s), epilogue, conclusion, afterword
 - backmatter: appendix, bibliography, endnote(s), glossary

## Useful links

 - [EPUB Packages 3.2](https://www.w3.org/publishing/epub32/epub-packages.html)
 - [EPUB Content Documents 3.2](https://www.w3.org/publishing/epub32/epub-contentdocs.html)
 - [EPUB 3 Structural Semantics Vocabulary](https://idpf.github.io/epub-vocabs/structure/)
 - [DCMI Metadata Terms](http://www.dublincore.org/specifications/dublin-core/dcmi-terms/)
