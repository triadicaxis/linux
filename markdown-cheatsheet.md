# Heading 1
## Heading 2
### Heading 3
#### Heading 4

---

Here is some **bold text** and some *italic text*.  
> Here is a block quote

Ordered list\:  

1. list item one
2. list item two
3. list item three

Unordered list\:  

- first item
- second item
- third item

[Link title](https://www.google.com)
![alt text](image.jpg)

Here's a sentence with a footnote. [^1] Here's another footnote. [^2]
And another footnote. [^3] And some `code` embedded in text.

[^1]: This is the first footnote.
[^2]: This is the second footnote.
[^3]: This is the third footnote.

To create a line break, end a line with two or more spaces and hit return. You also need to escape the following characters
\:

---

When finished writing in markdown, convert .md to .html using bash\:
```
  sudo apt-get update
  sudo apt-get install pandoc
```
Then from terminal\:
```
  pandoc -f markdown file.md > file.html
```  

Convert .md to .pdf from Atom\: `Packages > Markdown to PDF > Convert`


You can also convert .md to .pdf using bash\:
```
  pip install grip
  grip file.md
```
Then use Chrome's "Save as PDF" in the Print dialog.  
