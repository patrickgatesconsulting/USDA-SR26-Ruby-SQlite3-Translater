README
======

Import the USDA National Nutrient Database for Standard Reference into a
Sqlite3 database. Tested on ruby 1.9.2.

Instructions
------------

1. Download and the ASCII version of the SR26 database from the [Nutrient Data
Laboratory Home Page][ndl]. There is a 7.6 Mb ZIP file containing the entire
database.

2. Extract the database into this project's top-level directory. It will
create a subdirectory called 'sr26' and should look like:

        sr26/Data_src.pdf
        sr26/DATA_SRC.txt
        sr26/DATSRCLN.txt
        sr26/DERIV_CD.txt
        sr26/FD_GROUP.txt
        sr26/FOOD_DES.txt
        sr26/FOOTNOTE.txt
        sr26/LANGDESC.txt
        sr26/LANGUAL.txt
        sr26/NUT_DATA.txt
        sr26/NUTR_DEF.txt
        sr26/sr26_doc.pdf
        sr26/SRC_CD.txt
        sr26/WEIGHT.txt

3. Requires [bundler][bundler]. Run `bundle install` to install required gems
if needed.

4. Run `rake load` to create database and, optionally, `rake pivot` to create
a flattened table with nutrient values (pivot task requires [fts4][fts]
extensions to Sqlite).

[ndl]: http://www.ars.usda.gov/nutrientdata
[bundler]: http://gembundler.com/
[fts]: http://www.sqlite.org/fts3.html
