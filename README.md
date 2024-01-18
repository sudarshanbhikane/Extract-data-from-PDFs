# UiPath Project - Extract Data from Multiple PDFs

## Overview

This UiPath project is designed to  extraction of data from multiple PDF files. In this lesson, you will  utilize the Modern Get Text activity to extract specific information, including Invoice Number, Invoice Date, and Invoice Total, from native PDF files. The extracted data will then be organized and written into an Excel file.


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
