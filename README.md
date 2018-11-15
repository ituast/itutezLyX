# itutezLyX

Istanbul Technical University Thesis in LyX (UNOFFICIAL)

This is a LyX template/structure for Istanbul Technical University, Faculty of Engineering M.S. and Ph.D. Theses.

## What's New?
* Udpated to include ITU Earthquake Engineering and Disaster Management Institute

There are several things that need to be done before starting to use the template files.

1. Need to install `itutez.cls` and `itutez.bst` files to your LaTeX system.
2. Install `itutez.layout` file to LyX
3. Understand how `ch??LyX.lyx` files work.
4. Understand how input `*.tex` files work.
5. All files have to be UTF8 encoded. If it is LyX file, this has to be done from Settings > Language > Encoding.

## Installing `itutez.cls` and `itutez.bst` files

We will assume, you are using MikTeX on Windows

* Create a folder `localtexmf` on your hard drive on a convenient location. It is suggested that this folder is placed at root of any hard drive, e.g. `C:\localtexfm`.
* Create subfolders `tex` and `bibtex` under the folder `localtexmf`.
* Create subfolder `latex` under the folder `tex`.
* Create subfolder `bst` under the folder `bibtex`.
* Copy `itutez.cls` into the `latex` subfolder and `itutez.bst` file into the `bst` subfolder.
* Start MikTeX Console as admin.
* Under the "Settings" division, go to "Directories" tab.
* Add the `localtexmf` folder to the list of directories.
* Go to "Tasks" menu and click "Refresh filename database"
* The  `itutez.cls` and `itutez.bst`  should be recognized by MikTeX.

## Installing `itutez.layout` file

We will assume you are running LyX version 2.3.1-1

* Copy `itutez.layout` file to `\LyX-Main-Folder\Resources\layouts` folder
* Start LyX and Click "Reconfigure" under the "Tools" menu.
* Restart LyX.
* ITU Thesis Layout should appear at "Document" menu, "Document Settings," "Document Class" section, "Document Class" list, "Reports" section as "ITU Tez".

The main LyX file for the thesis is `tezLyX.lyx`. You should export to "PDF (pdflatex)" to see if everyhing works fine. A fully working package is provided, so you should see a sample PDF generated. Then you can edit your files as explained below to write your thesis.

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