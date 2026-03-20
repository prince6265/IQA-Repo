## interview Question extracted in 2026...
### 1. Count the distinct even numbers in the array
- First I iterate through the array and check if the number is even. Then I check whether the same number appeared earlier in the array using another loop. If it did not appear earlier, I increase the count. This ensures only distinct even numbers are counted without using any built-in methods.
```C#
int[] arr = { 2, 4, 6, 2, 8, 4, 10, 3, 5 };

int count = 0;

for (int i = 0; i < arr.Length; i++)
{
    // check if even
    if (arr[i] % 2 == 0)
    {
        bool isDuplicate = false;

        // check if this number appeared earlier
        for (int j = 0; j < i; j++)
        {
            if (arr[i] == arr[j])
            {
                isDuplicate = true;
                break;
            }
        }

        // count only distinct even numbers
        if (!isDuplicate)
        {
            count++;
        }
    }
}

Console.WriteLine("Distinct even numbers count: " + count);
```
### 2. Replace null with the previous integer, if the array starts with null take the last occured integer value from the array.
- First I find the last non-null value in the array. Then I iterate through the array. If the element is null and it's the first index, I replace it with the last value. Otherwise, I replace it with the previous element. This ensures all null values are filled correctly.
```C#
int?[] arr = { null, 2, null, 5, null, null, 8 };

// find last occurring integer
int lastValue = 0;
for (int i = arr.Length - 1; i >= 0; i--)
{
    if (arr[i] != null)
    {
        lastValue = arr[i].Value;
        break;
    }
}

// replace null values
for (int i = 0; i < arr.Length; i++)
{
    if (arr[i] == null)
    {
        if (i == 0)
            arr[i] = lastValue;
        else
            arr[i] = arr[i - 1];
    }
}

// print result
for (int i = 0; i < arr.Length; i++)
{
    Console.Write(arr[i] + " ");
}
```
### 3. Findout the all possible substring in the string "ABC".
- To find all substrings, iterate through the string using two loops. The outer loop selects the starting index and the inner loop generates substrings by expanding the end index.
```C#
string str = "ABC";

for (int i = 0; i < str.Length; i++)
{
    string sub = "";

    for (int j = i; j < str.Length; j++)
    {
        sub = sub + str[j];
        Console.WriteLine(sub);
    }
}
```
### 4. What is Auto mapper.
- AutoMapper is a library used in ASP.NET Core / C# applications to automatically map data from one object to another object.
- AutoMapper is a .NET library used to map objects from one type to another automatically. It is commonly used to map entities to DTOs in ASP.NET Core applications, reducing manual property mapping code.
### 5. Bug scenario you have 500 clients and web used by them is same but some client is facing a issue. lie there are entering correct address in the input field but the address is showing is different this problem occuring with only 30 % of the client. how you debug the scenario.
> Check API Request (Use browser Network tab.)
- Open Developer Tools
- Go to Network
- Capture the API request
- What address is sent to the API
- What address is returned by the API
> Check Browser / Cache Issues (Since only 30% users are affected, it might be)
- Browser cache
- Old JavaScript files
- CDN caching
- Hard refresh (Ctrl + F5)
- Clear browser cache
- Test in another browser
> Add Logging at Backend Side
### 6. Prepare entity like name, Address, salary, write a linq query to show the name of the employee who has salary more than 50000.
> Step 1 : Employee Entity
```C#
public class Employee
{
    public string Name { get; set; }
    public string Address { get; set; }
    public decimal Salary { get; set; }
}
```
> Step 2 : Inserting Data into the employee entity 
```
List<Employee> employees = new List<Employee>()
{
    new Employee { Name = "Rahul", Address = "Delhi", Salary = 45000 },
    new Employee { Name = "Amit", Address = "Mumbai", Salary = 60000 },
    new Employee { Name = "Priya", Address = "Bhopal", Salary = 70000 },
    new Employee { Name = "Rohit", Address = "Pune", Salary = 30000 }
};
```
> Step 3 : Linq Query to fetch employee who has salary more than 50,000
```C#
var result = from emp in employees
             where emp.Salary > 50000
             select emp.Name;

foreach (var name in result)
{
    Console.WriteLine(name);
}
```
### 7. Why we use callBack at API.
- Server calls the client back when work is finished.
- In APIs, a callback is used when the server needs to notify the client after some processing is completed, instead of the client continuously asking the server for the result.
### 8. Status property with view child in Angular.
- In Angular, @ViewChild is used to access a child component, directive, or DOM element from the parent component.
- When working with forms, developers often use status property to check the validation state of a form or control.
> The status property usually returns:
```
VALID
INVALID
PENDING
DISABLED
```
### 9. Use of Static keyword.
- In C#, the static keyword is used to declare members that belong to the class itself rather than to an instance (object) of the class.
- This means you can access them without creating an object.
```C#
static class Utility
{
    public static void ShowMessage()
    {
        Console.WriteLine("Hello");
    }
}
Utility.ShowMessage();
```
### 10. On a button click call one api once the first api get called then call the second API, so second API call is dependent on first one. with error handling in Angular
- In Angular, when the second API depends on the result of the first API, the common approach is to use RxJS operators like switchMap, concatMap, or mergeMap.
For dependent calls, switchMap or concatMap is usually used.
> Service API Calls
```TS
import { HttpClient } from '@angular/common/http';
import { Injectable } from '@angular/core';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class ApiService {

  constructor(private http: HttpClient) {}

  getUser() {
    return this.http.get('https://api.example.com/user');
  }

  getUserOrders(userId: number) {
    return this.http.get(`https://api.example.com/orders/${userId}`);
  }
}
```
> Compnent Logic - Dependent API Calls
```TS
import { Component } from '@angular/core';
import { ApiService } from './api.service';
import { switchMap, catchError } from 'rxjs/operators';
import { of } from 'rxjs';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html'
})
export class AppComponent {

  constructor(private apiService: ApiService) {}

  loadData() {

    this.apiService.getUser()
      .pipe(
        switchMap((user: any) => {
          return this.apiService.getUserOrders(user.id);
        }),
        catchError(error => {
          console.error("API Error:", error);
          return of(null);
        })
      )
      .subscribe(result => {
        console.log("Second API Response:", result);
      });

  }
}
```
> Flow Explanation
```
Button Click
     ↓
First API Call (getUser)
     ↓
Get user.id
     ↓
Second API Call (getUserOrders)
     ↓
Display result
```
### 11. Number of parameters we have to pass in httpClient, Angular
- In Angular, the HttpClient methods usually take two main parameters, but some methods can accept three parameters depending on the HTTP method.
> Basic Syntax of HttpClient
```TS
http.method(url, body?, options?)
```
> So there can be maximum 3 parameters.

| Parameter | Description                        |
| --------- | ---------------------------------- |
| url       | API endpoint                       |
| body      | Data sent to server (for POST/PUT) |
| options   | Headers, params, response type etc |

> Summary Table

| HTTP Method | Parameters         |
| ----------- | ------------------ |
| GET         | url, options       |
| POST        | url, body, options |
| PUT         | url, body, options |
| DELETE      | url, options       |

- In Angular HttpClient, methods usually accept two to three parameters. The first parameter is the API URL, the second is the request body (for POST or PUT), and the third is the options object which can include headers, query parameters, and other configurations.

### 12. Self join query to manager and employee.
- A Self Join is used when a table references itself.
```SQL
SELECT 
    e.Name AS EmployeeName,
    m.Name AS ManagerName
FROM Employee e
LEFT JOIN Employee m
ON e.ManagerId = m.EmpId;
```
- A self join is used when a table joins with itself. In the employee-manager scenario, both employees and managers are stored in the same table, so we create two aliases of the same table and join them using ManagerId and EmpId.
### 13. SQL Query to find duplicate employee.
- To find duplicate records in SQL, we use GROUP BY with HAVING COUNT(*) greater than 1. GROUP BY groups the records based on selected columns, and HAVING filters the groups that appear more than once.
```SQL 
SELECT Name, Email, COUNT(*) AS DuplicateCount
FROM Employee
GROUP BY Name, Email
HAVING COUNT(*) > 1;
```
### 14. give me the no of dupicate employee and there occurance.
```SQL
SELECT Name, COUNT(*) AS Occurrence
FROM Employee
GROUP BY Name
HAVING COUNT(*) > 1; 
```
### 15. Delete the duplicate records keep one of them.
- To delete duplicate records but keep one record, the common approach is to use ROW_NUMBER()
- To delete duplicate records while keeping one record, we use the ROW_NUMBER() function with PARTITION BY to identify duplicates. Then we delete rows where the row number is greater than 1.
```SQL
SELECT *,
ROW_NUMBER() OVER(PARTITION BY Name, Address, Salary ORDER BY EmpId) AS RowNum
FROM Employee;
```
```SQL
WITH CTE AS
(
    SELECT *,
    ROW_NUMBER() OVER(PARTITION BY Name, Address, Salary ORDER BY EmpId) AS RowNum
    FROM Employee
)

DELETE FROM CTE
WHERE RowNum > 1;
```

### 16. Temporary table and there synatax.
- A Temporary Table is a table that exists temporarily during a database session and is automatically deleted after the session ends.
- Temporary tables are commonly used in databases like Microsoft SQL Server for storing intermediate results during query execution.
- A temporary table is a table stored in tempdb that exists only for a limited time. It is mainly used to store intermediate data during query execution. In SQL Server, temporary tables can be local (#TableName) or global (##TableName).
> Local Temporary Table
```SQL 
CREATE TABLE #TempEmployee
(
    Id INT,
    Name VARCHAR(50),
    Salary INT
);
```
> Create Temporary Table Using SELECT
```SQL 
SELECT Name, Salary
INTO #TempEmp
FROM Employee;
```
> Global Temporary Table
```SQL
CREATE TABLE ##GlobalEmployee
(
    Id INT,
    Name VARCHAR(50)
);
```
### 17. What is local and global temporary table. In the context of session access.
- In SQL Server, a local temporary table is accessible only within the session that created it and is prefixed with a single #. A global temporary table is accessible to all sessions and is prefixed with ##. The local table is deleted when the session ends, while the global table is deleted when all sessions referencing it are closed.
