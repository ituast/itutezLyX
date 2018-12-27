# itutezLyX

Istanbul Technical University Thesis in LyX (UNOFFICIAL)

This is a LyX template/structure for Istanbul Technical University, Faculty of Engineering M.S. and Ph.D. Theses. It is derived from the original thesis template prepared by the Institute of Informatics of ITU.

## What's New

27 December 2018

* Renamed the files with `LyX` extension, so that it will not be confused with the original ITU LaTeX class.
* Updated the symbol table to use `longtable` so that it can extend mulpile pages automatically.
* Fixed the spacing for figure and table lists headers.
* Reorganized the preamble.

28 November 2018

* Udpated to include ITU Earthquake Engineering and Disaster Management Institute

## Steps to Follow

There are several things that need to be done before starting to use the template files.

1. Need to install a TeX system, LyX and supporting programs such as Jabref, SumatraPDF and etc...
1. Need to install `itutezLyX.cls` and `itutezLyX.bst` files to your LaTeX system.
1. Install `itutezLyX.layout` file to LyX.
1. Some adjustment to LyX PDF-PNG graphics converter for viewing PDF figures from LyX.
1. Understand how chapter files (`ch??LyX.lyx`) work.
1. Understand how input `*.tex` files work.
1. All files have to be UTF8 encoded. If it is LyX file, this has to be done from Settings > Language > Encoding.

## Suggested Software to Install (for Windows)

* MikTeX: a LaTeX system for Windows. Other OSs are also supported.
* LyX: A visual tool for LaTeX files
* JabRef: BibTeX and BibLaTeX bibliography editor
* TeXMaker: A LaTeX editor
* Notepad++: Extended editor for programming
* ImageMagick: Image processing libraries, need to install convert tool
* PDF XChange Pro: Licensed PDF tool for editing PDFs
* Sumatra PDF: PDF viewer suitable for LaTeX documents
* Cisco VPN: VPN to connect ITU network

## Installing `itutezLyX.cls` and `itutezLyX.bst` files

We will assume, you are using MikTeX on Windows

* Create a folder `localtexmf` on your hard drive on a convenient location. It is suggested that this folder is placed at root of any hard drive, e.g. `C:\localtexfm`.
* Create subfolders `tex` and `bibtex` under the folder `localtexmf`.
* Create subfolder `latex` under the folder `tex`.
* Create subfolder `bst` under the folder `bibtex`.
* Copy `itutezLyX.cls` into the `latex` subfolder and `itutezLyX.bst` file into the `bst` subfolder.
* Start MikTeX Console as admin.
* Under the "Settings" division, go to "Directories" tab.
* Add the `localtexmf` folder to the list of directories.
* Go to "Tasks" menu and click "Refresh filename database"
* The  `itutezLyX.cls` and `itutezLyX.bst`  should be recognized by MikTeX.

## Installing `itutezLyX.layout` file

We will assume you are running LyX version 2.3.1-1

* Copy `itutezLyX.layout` file to `\LyX-Main-Folder\Resources\layouts` folder
* Start LyX and Click "Reconfigure" under the "Tools" menu.
* Restart LyX.
* ITU Thesis Layout should appear at "Document" menu, "Document Settings," "Document Class" section, "Document Class" list, "Reports" section as "ITU Tez".

## Some adjustments to LyX PDF previewer

It is recommended that only PDF files are used for plots. Default LyX will show the PDFs with lower quality on the screen, when scaled. To solve this problem you need to tell to increase the resolution of the preview image as follows:

* Make sure the convert utility of ImageMagick is installed and made available to path.
* Start LyX and do not open a file.
* Go to "Preferences" under the "Tools" menu.
* Go to "Converters" under the "File Handling" section.
* Select "PDF(graphics)" from "From Format:" and "PNG" from "To Format:"
* To "Converter:" write : `convert -density *** -trim -quality 100 -sharpen 0x1.0 $$i $$o`, where *** can be 200 to start with. You may try other values based on the results.
* Click "Add" button.
* Click "Apply" button.
* Click "Save" button.
* Select "Reconfigure" under "Tools" menu.
* Restart LyX.

## Verification

The main LyX file for the thesis is `tezLyX.lyx`. You should export it to "PDF (pdflatex)" to see if everyhing works fine.

A fully working package is provided, so you should see a sample PDF generated. Then you can edit your files as explained below to write your thesis.

## How to Write Thesis

First of all, you can start by writing your chapters in LyX. From the main LyX file click to one of the chapters, and select "Edit". This will open up the corresponding chapter. You can now write your thesis chapter.

You will see that there are examples for figures, bibliography and tables. You can use you these formats or a format you prefer. However, it is strongly recommended that you export to PDF frequently to make sure your custom figure or table works fine.

You should change the bibliography as needed. Software such as [JabRef](http://www.jabref.org/) is recommended for editing the bibliography.

Other files that need to be completed are:

* `kisaltmalarLyX.lyx`
* `onsozLyX.lyx`
* `ozetLyX.lyx`
* `ozgecmisLyX.lyx`
* `sembollerLyX.lyx`
* `summaryLyX.lyx`

These are LyX files but the main LyX file will look for their `*.tex` versions. Therefore, they need to be converted to LaTeX as follows:

* Export the `*.lyx` file to "LaTeX (pdflatex)."
* Edit the exported `*.tex` file and erase the parts above and including `\begin{document}` and erase the last line `\end{document}`.

Before making cahnges to the `*.tex` files, it is highly recommended that you save the existing files first, look at them and see how they are formatted. Some of the `.tex` files are simple text files without any LaTeX code in it (e.g `onsozLyX.tex` file); so for those, you do not need to work in LyX; just modify the `*.tex` file with a text editor.

Also note that `*.tex` files are called in the main LyX file at "Document" menu, "Document Settings," "LaTeX Preamble" section. If you like, you can change the names of these files as needed.

## Questions

For questions, please contact to [Baris Erkus](mailto:bariserkus@itu.edu.tr)