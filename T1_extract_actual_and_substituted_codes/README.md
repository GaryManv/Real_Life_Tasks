# Extract Specific Strings <br>

#### Task: <br>
Substituted items exist in the Product Data of Oracle ERP. An output report in a text file presents both substituted and actual products.<br>
The task is to extract the codes of substituted and actual products and return a table with the superseded product codes in the first column and the actual part numbers in the other column.

#### Step 1 : Data observation <br>
*  Data stored in "Supersided.txt" file.<br>
*  The strings we need (codes) are located in text lines with "Item: ", "Yes",and  "No"<br>
*  Supersided Item Code is always starts with "Item: " and located in the begining of the textline<br>
*  Actual Item Code is always in the begining of the textline.<br>
*  Codes are numerical, alphabetical, some include spaces as well as other simbols.<br>
*  Substituded code is repeated when there is no enough space on the page for the actual code. <br>
*  The gap between different sections of strings in textline made of more than one spaces.<br>
*  One substitided code can refer to many actual codes.<br>

#### Step 2: Realization<br>
*  Filter lines by removing leading and trailing whitespaces,replace single spaces with no spaces and selecting lines containing "Item:", "No", or "Yes"<br>
*  Split filtered lines into segments based on spaces<br>
*  Create a new list with inner lists containing the first elements from split segments<br>
*  Creating dataframe (62152 rows) <br>
*  Remove duplicated rows (8512 unique rows) <br>
*  Saving in csv file ('BLY_SUBS_2_columns.csv') <br>

#### Step 3: Observation of results<br>




