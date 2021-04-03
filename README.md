# KiCad-NetlistToBOM
Exporting Bill-Of-Materials from KiCad to CSV properly

I made a custom plugin to KiCad with Python that can be used to export BOM from KiCad netlist. KiCad has nice feature that there is possibility to add custom fields to netlist for every component. This code works with custom fields named "MPN" for Manufacturer Part Number and "Description" for part description. It also uses reference designator fields and combines them automatically when the values fields matches.

Output is formatted to conforms Eurocircuits requirements, but it is easy to modify when needed. User needs only import that CSV to LibreOffice Calc and save it to XLS file. For some reason Eurocircuits is using Micro$oft proprietary file format for that purpose. But I can live with that. I don't want to use any software from that company.

There is no need to fill MPN or description fields to every similar component. Plugin takes first non-null field and copies it to resulting CSV to that component group.

CSV is in it's standard form. Separated with semi-colon and only non-numeric fields are quoted.

Save this file to KiCad plugins folder.

You can freely use and edit this code. Enjoy!
