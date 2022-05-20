# SFLC.in-Task

Source Code File:  [[https://github.com/prachi237/SFLC.in-Task/blob/master/csv-warnReport.csv](https://github.com/prachi237/SFLC.in-Task/blob/master/dataAbstraction_Code.ipynb)](dataAbstraction_Code.ipynb)
<br> CSV File Obtained: [https://github.com/prachi237/SFLC.in-Task/blob/master/csv-warnReport.csv](csv-warnReport.csv)


To extract the table data from the pdf in an automated way to a panda dataframe or CSV the steps in brief that I followed are as follows:

* Installed Pandas and Tabula Library
  
  ```
  pip install tabula-py
  pip install pandas
  ```
  
* Imported Pandas and Tabula
  ```
  import pandas as pd
  import tabula
  ```
* Converted the PDF into DataFrame

  ```
  file = "ca-warn-report.pdf"
  dataFrame = tabula.read_pdf(file,pages='all')
  ```

* Testing/Viewing the dataframe
  ```
  dataFrame
  ```
  You can check page wise by writing the command dataFrame[page_no] e.g: dataFrame[0]
  
* Used Tabula Library to scrape the tables from the given PDF file and convert those to CSV file
  ```
  tabula.convert_into("ca-warn-report.pdf", "csv-warnReport.csv", output_format="csv", pages='all')
  ```


