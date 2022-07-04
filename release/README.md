Release Instructions Notes
==========================

**General editing between releases**

- Currently uses v6.0.4 of KiKad
- Open it to do all editing
- Once done with edits
- Before commiting changes use ***Inspect > Design Rules Checker (DRC)*** and review acceptable warnings

**For each release follow these steps**

- Make sure to update either the schematic version or PCB version (on silkscreen) or both accordingly
- Run the DRC (see above) - make sure no errors and only acceptable warnings
- All files from the follow three steps should update all files in ```/release```
- Run **File > Fabrication Outputs > Generate Gerbers** and select the ```/release``` directory and click Plot
- From the same dialog as above click **Generate Drill Files...**
- Run **File > Fabrication Outputs > Component Placement** click button generate .pos files
- Update ```BOM.csv``` as needed
- Commit changes as normal and create a GitHub Release record

**Current Acceptable Warnings**

- Currently for PCB v.04 there are only 6 warnings relating silkscreen overlap with pads