# Digital Latin Library Engelmann Project
This repository contains raw data files for a project to catalog all of the entries in Wilhelm Engelmann's *Bibliotheca Scriptorum Classicorum*, volume 2: Scriptores Latini (Leipzig 1882) for inclusion (eventually) in the Digital Latin Library's [catalog](https://catalog.digitallatin.org).

Undergraduate research assistants Alexander Konieczny, Rachel Rucker, and Ana Oaxaca have combed through the printed version of Engelmann's work and searched a variety of online resources for digital versions of the editions in it. They kept track of entries using [Zotero](https://www.zotero.org/). The raw data is available in this repository as a Zotero RDF file (`Engelmann.rdf`). Many works do not exist in a digital format; those works are listed in the file `Works-Not-Found.odt`. If you know of any digital versions of those works, contact Samuel J. Huskey at [huskey@ou.edu](mailto:huskey@ou.edu)

## Instructions for Student Workers
This repository includes three versions of the Zotero data in CSV form:
* Engelmann.csv, which is the master file,
* Engelmann-AK.csv, which is Alexander's copy,
* Engelmann-RR.csv, which is Rachel's copy.

Your job is to reconcile the data in certain columns of your copy of `Engelmann.csv` with authority records from the DLL Catalog's database.

Each copy of `Engelmann.csv` includes the columns `Author`, `Title`, and `Editor`, all of which contain data from the Zotero collection that you compiled. Since that data originated in a variety of resources, there are variations in spelling, language, punctuation, etc., between the different entries. It is important to preserve that data, but we also need to have a standard way of referring to it. That is why we have authority records from the DLL's Catalog.

If you decide to sort the data in your copy of `Engelmann.csv`, be sure to select _all_ of the columns and rows before you execute a sort command. Otherwise, your data will become unorganized and, consequently, of little use.

### General Procedures
Use Git to clone this repository onto your computer so that you will have your own copy of the files to edit.

Work only on the column(s) assigned to you.

At the beginning of every working session, execute `git pull` to obtain the most recent version of the files in the repository.

After you have finished a session:
1. Execute `git add .` to stage your work.
2. Execute `git commit -m` and add a brief message about what you did during the session.
3. Execute `git push` to push your changes to the remote repository.

You may also use the Git features incorporated into the Atom editor or the GitHub desktop application to accomplish these tasks. It is a good idea to execute the Git routine enumerated above before you do any sorting so that you can always revert your changes to a previous version, if necessary.

#### Authors and Editors
The data in the `Author` and `Editor` columns in your copy of `Engelmann.csv` should have corresponding authorities in the file `dll-author-authorities.csv`, which has one author record per row, with multiple versions of each author's name in the columns. The column `DLL Author Record` contains the data that you will copy and insert into the column `DLL Author Name` in your copy of `Engelmann.csv`.

Working from the top of the spreadsheet downwards, search for a match of the name in the `Author` or `Editor` column in your copy of `Engelmann.csv` in the `DLL Author Record` column in `dll-author-authorities.csv`. When you find a match, copy and paste it into the `DLL Author Name` column in your copy of `Engelmann.csv`.

If there is more than one author for the record, insert a semicolon (;) between the names. Do not leave a space between the semicolon and the next name.

If you cannot find a match, make a note (including the value from the `Key` column for the record(s) in your copy of `Engelmann.csv`) in a separate file and confer with Dr. Huskey.

#### Titles
The data in the `Title` column in your copy of `Engelmann.csv` should have corresponding authorities in the file `dll-work-authorities.csv`, which has one work per row, with author and title information in separate columns. The column `DLL Work Record` contains the data that you will copy and insert into the column `DLL Title` in your copy of `Engelmann.csv`.

For the records that have specific titles, the task is relatively easy: search for a matching value in `dll-work-authorities.csv` and copy the `DLL Work Record` value into your copy of `Engelmann.csv`. Unfortunately, many records have generic titles such as *Opera* or *Carmina*. In those cases, you will need to copy the value of the `Url` column, paste it into the address bar of a browser, and scroll through the work to identify all of the titles that it contains. Match those titles with records in `dll-work-authorities.csv` and copy and paste the values into `DLL Title` in your copy of `Engelmann.csv`, separating the titles with a semicolon (;) and no space.

If you cannot find a match, make a note (including the value from the `Key` column for the record(s) in your copy of `Engelmann.csv`) in a separate file and confer with Dr. Huskey.
