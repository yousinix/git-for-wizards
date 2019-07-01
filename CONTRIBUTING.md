# Contribute to *Git for Wizards*

<!-- TOC depthFrom:2 -->

- [1. Sections Naming](#1-sections-naming)
- [2. Commit Message](#2-commit-message)
    - [2.1. New Sections](#21-new-sections)
    - [2.2. New Spells](#22-new-spells)
- [3. Formating](#3-formating)
    - [3.1. Markdown Rules](#31-markdown-rules)
    - [3.2. Title Case](#32-title-case)
    - [3.3. Sections Numbering](#33-sections-numbering)
    - [3.4. TOC](#34-toc)
- [4. References](#4-references)

<!-- /TOC -->

## 1. Sections Naming

Spells should have names inspired from **magic spells** like the [ones](https://www.pottermore.com/collection/spells-and-charms) used in J.K. Rowling's _Harry Potter_ or any other similar alternative.

## 2. Commit Message

### 2.1. New Sections

```txt
Add {SECTION_NAME} Section
```

**Example**

```txt
Add Markdown Beautifio Section
```

### 2.2. New Spells

```txt
Add {NUMBER} New Spells to {SECTION_NAME}

 * {SPELL_NAME}
 * {SPELL_NAME}
```

**Example**

```txt
Add 2 New Spells to Markdown Beautifio

 * Keyboard Key Strokes
 * Mathematics Equations
```

## 3. Formating

### 3.1. Markdown Rules

- Follow these [rules](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md) while writing markdown.
- Use [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) for Markdown linting and style checking in Visual Studio Code.

### 3.2. Title Case

- When writing a name or a title, it is a common convention to only use **capital letters** to start the principal words.
- **Non-principal** words are written with a **lowercase** letter unless they start the title.
- Non-principal words:
    1. Articles _(a, an, the, etc.)_
    1. Conjunctions _(and, but, or, etc.)_
    1. Prepositions _(on, in, with, etc.)_

### 3.3. Sections Numbering

- Use [Markdown TOC](https://marketplace.visualstudio.com/items?itemName=AlanWalk.markdown-toc) to update **Sections Numbering** after adding new section or spell.

### 3.4. TOC

- Use [Markdown TOC](https://marketplace.visualstudio.com/items?itemName=AlanWalk.markdown-toc) to update **Table of Contents** after adding new section or spell.
- Sections name is written in **BOLD**.

## 4. References

- References should always be cited in the **References and Acknowledgments** section at the end of the `README.md` file.
- Cited references should be arranged in **alphabetical order**.
