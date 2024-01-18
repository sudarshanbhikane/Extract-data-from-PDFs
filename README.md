# UiPath Project - Extract Data from Multiple PDFs

## Overview

This UiPath project is designed to enhance your skills by practicing the extraction of data from multiple PDF files. In this lesson, you will learn to utilize the Modern Get Text activity to extract specific information, including Invoice Number, Invoice Date, and Invoice Total, from native PDF files. The extracted data will then be organized and written into an Excel file.

## Duration

Approximately 20 minutes

## Learning Objectives

By the end of this lesson, you should be able to:

1. Extract data from multiple PDFs using the Modern Get Text activity.
2. Build a workflow to extract Invoice Number, Invoice Date, and Invoice Total from PDFs.
3. Utilize variables, input and output activities, and basic calculations in UiPath.

## Prerequisites

- Download the PDF Exercise Resource.zip (103.8 KB) provided with this lesson.

## Getting Started

### Your Turn

This exercise presents a valuable opportunity to refine your UiPath skills through hands-on practice. Engage with variables, input/output activities, and basic calculations to successfully complete the task.

![Your Turn](Your_Turn_NOPROCESS_.png)

## Project Files

### Exercise Resources

- [PDF Exercise Resource.zip](PDF%20Exercise%20Resource.zip) (103.8 KB)


## Solution Steps

1. **Download PDF Files:**
   - Download the PDF files and place them in the `Invoice` folder within the Project directory.

2. **Sequence Renaming:**
   - Rename the main sequence for clarity and add a descriptive annotation.

3. **Assign Activity for Folder Path:**
   - Use an Assign activity to obtain the invoice file paths from the designated folder.
   - Save the path into a string variable named `FolderPath`.

4. **Build Data Table:**
   - Add a Build Data Table activity.
   - Create a Data Table with columns for Invoice Number, Invoice Date, and Invoice Total.
   - Save the output as `dt_InvoiceDetails`.

5. **PDF Processing Loop:**
   - Add a For Each File in Folder activity to iterate through the PDF files.
   - Utilize Use Application/Browser activity to open PDF files in Adobe Acrobat Reader.
   - Add Get Text activities to extract data containing Invoice Number, Invoice Date, and Invoice Total.
   - Use Assign activities to refine and process the extracted data.
   - Utilize Add Data Row activity to store the extracted data in `dt_InvoiceDetails`.

6. **Excel Reporting:**
   - Use Write Range Workbook to write the data into an Excel file.
   - Provide the workbook path as "Invoice Details.xlsx".
   - Set the sheet name as "Sheet1" and designate "A1" as the starting cell.
   - Check the "Add Headers" option under Options in the Properties Panel.
   - Populate the Excel file with data from `dt_InvoiceDetails`.

Feel free to explore and enhance the solution by incorporating additional fields or refining the workflow further. Happy automating!
