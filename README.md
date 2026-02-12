 PDF Bookmark Editor (chrome, firefox, edge)

 https://mrfragger.github.io/pdf-bookmark-editor/

- Add / Edit bookmarks for a PDF
- add chapter, section or subsection bookmarks
- select text in pdf to use for bookmark title
- load existing bookmarks
- import or export bookmarks to a text file
- grayscale (default), dark and light modes
- zoom in/out and zooms to page width by default
- Titlelize chapter titles Aa (see example below)
- Who is the author of the treatise?
- Who Is the Author of the Treatise?
- merge PDFS retaining existing bookmarks
- rearrange order of PDFs to merge
- rotate, delete pages
- select all, none, even, odd, invert
- select ranges 22-34, 38, 42, 44-56
- visually drag page thumbnails to reorder
- undo multiple times
- minisearch multi term search, bm25
- ranking score search results
- since most PDF viewers only allow searching on one term
- PWA (progressive web app), installs offline
- Librewolf/Firefox bookmark and it'll be cached

![](pdfbookmarkeditor.jpg)
![](pdfbookmarkpages.jpg)

 There should be a free PDF editor for bookmarks without ads, freemium or a subscription.  I looked but never could find one.  Just a few python command line ones that work great for advanced users. This app is all local.  No cdn (content delivery networks) either just 5 files loaded ~3MB total.
 ```
index.html 120KB
pdf.worker.min.js 1.1MB
pdf-lib.min.js 525KB
pdf.min.js 320KB
index.min.js 19KB
```
Doesn't do vertical position (jumping to exact location of text in a page) within PDFs (as that requires pymupdf and python) but allows one to easily modify bookmarks for pages. Crop function isn't practical in this app nor is  a compression function since that requires ghostscript (gs).  For annotation, adding text, highlightning open PDF in Firefox.

### Use Ghostscript (free AGPL) for PDF compression:
```bash
brew install gs         sudo apt install gs      choco install gs

# /screen smallest size (72 dpi, lower quality) or /ebook balance size and quality (150 dpi) or /printer high quality (300 dpi)
gs -sDEVICE=pdfwrite -dPDFSETTINGS=/screen -dNOPAUSE -dBATCH -sOutputFile=compressed.pdf input.pdf
```


