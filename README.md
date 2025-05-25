# Python-I/o
```js
name = input("Whats Your name?")
print(f"hello, {name}")
```
```js
names = []
for _ in range(3):
    names.append(input("whats your name?"))
    for name in sorted(names):
        print(f"hello,{name}")
```

```js
name = (input("whats your name?"))
file = open("names.txt","w")
file.write(name)
file.close()
```
```js
name = input("What's your name? ")
with open("names.txt", "a") as file:
    file.write(f"{name}\n")
```
```js
with open("names.txt", "r") as file:
    lines = file.readlines()
for line in lines:
    print("hello,",line , end="")  print("hello,",line.rstrip())    
```
```js
with open("names.txt", "r") as file:
 for line in file:
  print("hello,",line.rstrip())    
```
```js
names = []
with open("names.txt") as file:
    for line in file:
        names.append(line.rstrip())
for name in sorted(names):
    print(f"hello, {name}")        
```
```js
with open("names.txt") as file:
    for line in sorted(file):
      print("hello,",line.rstrip())        
```
```js
names.csv ALi,70%
ROn,80%
JOe,40%
Doe,30%
Aloha,55%

syudents.py 
with open("names.csv") as file:
    for   line in file:
        row = line.rstrip().split(",")
        print(f"{row[0]} has  {row[1]} total")   
```
```js
with open("names.csv") as file:
    for   line in file:
        name, number = line.rstrip().split(",")
        print(f"{name} has  {number} total")   
```
```js
students = []

# Read data from the CSV file and populate the students list
with open("names.csv") as file:
    for line in file:
        name, number = line.rstrip().split(",")
        student = {"name": name, "number": number}
        students.append(student)

# Function to sort by student name
def get_name(student):
    return student["name"]

# Sort students by name using the key function and print them
for student in sorted(students, key=get_name):
    print(f"{student['name']} got {student['number']}")

```
```js
students = []

# Read data from the CSV file and populate the students list
with open("names.csv") as file:
    for line in file:
        name, number = line.rstrip().split(",")
        student = {"name": name, "number": number}
        students.append(student)


# Sort students by name using the key function and print them
for student in sorted(students, key=lambda student: student["name"]):
    print(f"{student['name']} got {student['number']}")

```
```js
8:14
name,number
ALi,70%
ROn,80%
JOe,40%
Doe,30%
Aloha,55%
--------------------------------------------
# Import the csv module to easily read CSV files
import csv

# Create an empty list to store student dictionaries
students = []

# Open the CSV file named "names.csv"
with open("names.csv") as file:
    # Use csv.reader to read the file line by line
    reader = csv.reader(file)
    
    # Iterate over each row in the CSV file
    for name, number in reader:
        # Create a dictionary for each student and add it to the list
        students.append({"name": name, "number": number})

# Sort the list of students by the "name" key and print each one
for student in sorted(students, key=lambda student: student["name"]):
    print(f"{student['name']} got {student['number']}")

```
```js
# Import the csv module to work with CSV files
import csv

# Create an empty list to store student data
students = []

# Open the CSV file
with open("names.csv") as file:
    # Use DictReader to read the file into a dictionary for each row
    reader = csv.DictReader(file)
    
    # Loop through each row in the CSV file
    for row in reader:
        # Append each row as a dictionary with keys "name" and "number"
        students.append({"name": row["name"], "number": row["number"]})

# Sort the students list by name and print the results
for student in sorted(students, key=lambda student: student["name"]):
    print(f"{student['name']} got {student['number']}")

```
```js
import csv
name = input("What Your name?")
number = input("What is your number? ")
with open("names.csv","a") as file:
    writer = csv.writer(file)
    writer.writerow([name,number])
```
```js
import csv
name = input("What is your name? ")
number = input("What is your number? ")

with open("names.csv", "a+", newline='') as file:
    writer = csv.DictWriter(file, fieldnames=["name", "number"])
    
    # Write header if file is empty
    file.seek(0)
    if not file.read(1):
        writer.writeheader()
    writer.writerow({"name": name, "number": number})
```
```js
```
```js
```
