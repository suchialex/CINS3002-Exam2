<details>
  <summary>
    ✅ Create Pycharm Project
  </summary>

  - Add files main.py, classes.py, part1.py and part2.py
  - Download the [dictionary file](https://github.com/suchialex/CINS3002-Exam2/blob/main/employees.txt)
  - Download [pretty_print module](https://github.com/suchialex/pretty-print/blob/main/suchi_pretty_print.py)
  - All dictionary operations will be in a function in part1.py
  - Class will be defined in classes.py
  - All class operations will be in a fucntion in part2.py
</details>


# Part 1: (50 pts)
<details>
  <summary>
    Dictionary structure
  </summary>

- The employees dictionary has  
`integer` (employee ID) -> `dictionary`

  - "name" -> `string`
  - "dept" -> `string`
  - "salary" -> `float` or `int`
  - "projects" -> `set`
  - "titles" -> `list`
  - "certifications" -> `dictionary`
    - `string` (certfication code) -> `string` (date in YYYY-MM-DD)
</details>

## In part1.py

<details>
  <summary>
    Dictionary Operations - (50 pts + 5 Bonus pts)
  </summary>

<details>
<summary>
  ✅ 0. Unpickle dictionary (3.5 pts)
</summary>

- Unpickle the dictionary in the file employees.txt
- Must use exception handling
</details>
   

<details>
<summary>
 ✅ 1. Print managers (5 pts)
</summary>
  
  - Print the name, department, salary of all the employees who have `manager` as one of their titles
  - Perform a case-insensitive search on title
  - Must be in a nice tabular format
  - You may choose alignments and widths to fit the data
  - If name or department or salary are missing, print N/A
</details>


<details>
<summary>
 ✅ 2. Add title (5 pts)
</summary>

- Ask user for a name
- Add a new title `Developer` for any  employee with that name
- Perform a case-insensitive comparison of the name
</details>


<details>
<summary>
 ✅ 3. Add certification (5 pts)
</summary>

- Ask user for a new employee ID and
- if that employee is present in the dictionary,
- ask user to enter
  - new certification code and
  - date taken
- add these values to that employee's certifications
- Cert code must be all uppercase regardless of user input
- Assume user will give good value for date in YYYY-MM-DD format

<details>
  <summary>
    Bonus 5 pts
  </summary>

  Perform validation on date 
  - year must be between 1995 and 2025,
  - month must be between 1 and 12,
  - date must be between
    - 1 and 30 for Apr, June, Sep, Nov
    - 1 and 31 for Jan, Mar, May, Jul, Aug, Oct, Dec
    - 1 and 28 for Feb in non-leap years
    - 1 and 29 for Feb in leap years
</details>
</details>


<details>
<summary>
  ✅ 4. Mayfield Inc Employees (5 pts)
</summary>

  Print the name and salaries of all the employees who are working on the project Mayfield Inc. The project name comparison must be case-insensitive. Choose a nice format and alignment so they are displayed in a tabular fashion. If either name or salary not available, print -
</details>


<details>
<summary>
  ✅ 5. Salary Raise (5 pts)
</summary>

  For all the employees working on Spring Valley, give a 25% raise in their salary. If anyone doesn't have a salary, set their salary at 65000. Perform a case-insensitive search on projects.
</details>


<details>
<summary>
  ✅ 6. Add certification for IT employees (5 pts)
</summary>
  
  - Add a new certifcation `OCPL1` taken on `March 10, 2024` for all employees in the IT department
  - Perform case-insensitive search on department
  - Make sure the date is in the right format when you insert it in the dictionary
</details>



<details>
<summary>
  ✅ 7. Employees with multiple certifications (5 pts)
</summary>
  
  - Print the name, salary and department of all the employees with more than one certification
  - Must be in a tabular fashion, choose your alignments and widths to fit data
  - If name or salary or department not available, print -
</details>



<details>
<summary>
  ✅ 8. Add title for SCJP certified (5 pts)
</summary>
  
  - For anyone who has `SCJP` as one of the certifications, add a title called `Java Developer`
  - Perform case-insensitive search on cert code
</details>



<details>
<summary>
  ✅ 9. Employees missing name (5 pts)
</summary>
  
  - Check the dictionary for any employee who might be missing a name
  - and if missing, print their ID and
  - ask the user to provide a name
  - Validate this name so
    - it doesn't have any special characters except space
    - format it so that first letter of each word is uppercase.
  - You may implement it in a separate function named validate_name, or in this function itself
</details>

  
<details>
<summary>
  ✅ 0. (1.5 pts)
</summary>
  
  - Pickle this dictionary and save it in a file (choose a name for your file)
</details>

</details>


# Part 2: (50 pts)

## In classes.py

<details>
  <summary>
    Class Definition - (34 pts)
  </summary>

  1. Create a class named computer (code conventions must be followed)
  2. This class will have
     - three instance attributes (all private attributes)
       - price
       - RAM
       - HDD
     - one initializer method (5 pts)
     - one str method (5 pts)
     - three get methods (for each 
attribute) (12 pts)
     - three set methods (for each attribute) (12 pts)
  4. Define the initializer method to bind all the attributes to the object, you may choose attribute names
  5. Define the str method to display the state of your object (choose a nice format)
  6. Define three different get methods to access the price, RAM and HDD using the minimal statements needed
  7. Define three different set methods to change the values of the price, RAM and HDD, using the minimal statements needed
</details>


## In part2.py:

<details>
  <summary>
    Creating and manipulating objects using methods - (16 pts)
  </summary>

  1. Create an object of the class defined above (choose your variable name) with three string values - `1900.99, 16GB, 1TB` - (3 pts)
  2. Create a dictionary with key 'Apple' and value is the object created in step 1 - (2 pts)
  3. Create another object (choose your variable name) with three string values - `2999.99, 16GB, 2TB` - (3 pts)
  4. Add to the dictionary another element - key 'ApplePro' and value is the object created in step 3 - (2 pts)
  5. Write print statements that print the following:  
  `Apple - Price: $1900.99 - New Price: $1875.99`
  (4 pts)  
  💡 Hint: Use must use the object you created in Step 1, print the product key using the object (i.e. get the object's key from the dictionary), print its price using the accessor method, then use the mutator method to change the price, and print the new price again using the accessor method
  7. Serialize this dictionary (pickle it) and save it in a file (choose any name for the file) - (2 pts)
</details>
