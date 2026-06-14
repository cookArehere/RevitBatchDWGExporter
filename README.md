# RevitBatchDWGExporter
A pyRevit script for batch exporting sheets from multiple Revit models into clean, merged DWG files (AutoCAD 2007 format) via an interactive GUI.
# Revit Batch DWG Exporter (pyRevit)

A lightweight Python script for **pyRevit** designed to automate the tedious process of exporting sheets to DWG from multiple Revit files at once. It operates in the background, minimizing UI overhead and significantly speeding up the documentation release workflow.

## 🚀 Key Features

* **Batch Processing:** Automatically opens, processes, and closes all `.rvt` models within a selected folder.
* **Smart Backup Filtering:** Uses regex to automatically detect and skip Revit backup files (`*.####.rvt`), ensuring only main models are processed.
* **Clean Output (Merged Views):** Binds all views, schedules, and title blocks directly into a single, standalone DWG file per sheet—no messy external reference (Xref) file clutter.
* **Legacy CAD Support:** Forces exports into the **AutoCAD 2007** file format for maximum downstream compatibility with consultants and contractors.
* **User-Friendly GUI:** Powered by `pyrevit.forms` to provide intuitive folder picker dialogs for selecting source and destination paths, with graceful exit handling if cancelled.

## 🛠️ Prerequisites

* Autodesk Revit (Tested on Revit 2024)
* [pyRevit](https://github.com/eirannejad/pyRevit) environment installed and configured.

## 📦 Installation

1. Create a `.pushbutton` folder inside your custom pyRevit extension directory (e.g., `BatchExportDWG.pushbutton`).
2. Paste the script into a file named `script.py` inside that folder.
3. Add an `icon.png` (32x32) to the same directory.
4. Reload pyRevit.
