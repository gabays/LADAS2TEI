# LADAS2TEI<sup>geneva</sup>

This Python script transforms XML ALTO files, using [LaDaS layout analysis descriptions](https://github.com/DEFI-COLaF/LADaS), into TEI files.

## Install

```bash
git clone https://github.com/gabays/LADAS2TEI.git
cd LADAS2TEI
virtualenv -p python3.9 env #or later
source env/bin/activate
pip install -r requirements.txt
```

## Run the program

To run the program:

```bash
python ladas2tei.py [csv_file].csv
```

To run the example:
```bash
python ladas2tei.py  corpus/metadata.csv
```

## Preparing the data and the TEI

⚠️ The file names has to follow a specific format: `\w+_\d+.xml`: the program extract the number to organize sequentially the files.

A basic `<teiHeader>` is provided (`basic_header.txt`) but can be adapted. The metadata of the `<teiHeader>` are retrieved from the `[csv_file].csv` file.

To use a custom header, create a header pattern in a text file similar to the one in `pattern_colaf.txt`. You can include your own metadata fields in the CSV by placing their names in brackets in the pattern.

## Credits

The repo is adapted from the [LADAS2TEI repo](https://github.com/DEFI-COLaF/LADAS2TEI)