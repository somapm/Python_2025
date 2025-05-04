**Exercise 03**
**Question 01**
# Get input from user
first_string = input("Enter the first string: ")
second_string = input("Enter the second string: ")

# Check if second string is in first string
if second_string in first_string:
    # Remove all occurrences of second string
    result = first_string.replace(second_string, "")
else:
    # Add second string to beginning and end
    result = second_string + first_string + second_string

# Output the result
print("Result:", result)
**Question 02**
salary = float(input("Enter the employee's base salary: "))

if salary < 3000:
    tax_rate = 0.0
elif 3000 <= salary <= 5000:
    tax_rate = 0.10
elif 5000 < salary <= 8000:
    tax_rate = 0.15
else:  # salary > 8000
    tax_rate = 0.20

tax_amount = salary * tax_rate
net_salary = salary - tax_amount

print(f"Net salary after tax deduction: {net_salary:.2f}")
salary = float(input("Enter the employee's base salary: "))

if salary < 3000:
    tax_rate = 0.0
elif 3000 <= salary <= 5000:
    tax_rate = 0.10
elif 5000 < salary <= 8000:
    tax_rate = 0.15
else:  # salary > 8000
    tax_rate = 0.20

tax_amount = salary * tax_rate
net_salary = salary - tax_amount

print(f"Net salary after tax deduction: {net_salary:.2f}")
salary = float(input("Enter the employee's base salary: "))

if salary < 3000:
    tax_rate = 0.0
elif 3000 <= salary <= 5000:
    tax_rate = 0.10
elif 5000 < salary <= 8000:
    tax_rate = 0.15
else:  # salary > 8000
    tax_rate = 0.20

tax_amount = salary * tax_rate
net_salary = salary - tax_amount

print(f"Net salary after tax deduction: {net_salary:.2f}")
salary = float(input("Enter the employee's base salary: "))

if salary < 3000:
    tax_rate = 0.0
elif 3000 <= salary <= 5000:
    tax_rate = 0.10
elif 5000 < salary <= 8000:
    tax_rate = 0.15
else:  # salary > 8000
    tax_rate = 0.20

tax_amount = salary * tax_rate
net_salary = salary - tax_amount

print(f"Net salary after tax deduction: {net_salary:.2f}")
# Get the base salary from the user
salary = float(input("Enter the employee's base salary: "))

# Determine the tax based on salary range
if salary < 3000:
    tax_rate = 0.0
elif salary <= 5000:
    tax_rate = 0.10
elif salary <= 8000:
    tax_rate = 0.15
else:
    tax_rate = 0.20

# Calculate tax and net salary
tax_amount = salary * tax_rate
net_salary = salary - tax_amount

# Display the net salary
print(f"Net salary after tax deduction: {net_salary:.2f}")
**Exercise 04**
**Question 01**
# Collect information for 5 products
products = []

for i in range(5):
    name = input(f"Enter the name of product {i+1}: ")
    price = float(input(f"Enter the price of product {i+1}: "))
    products.append((name, price))

print("\nProduct Information:")
# Display each product with label
for name, price in products:
    label = "Expensive" if price > 500 else "Cheap"
    print(f"Product: {name}, Price: {price:.2f}, Label: {label}")

# Calculate average price
total_price = 0
for _, price in products:
    total_price += price
average_price = total_price / len(products)
print(f"\nAverage Price: {average_price:.2f}")

# Find the cheapest and most expensive product (without lambda)
cheapest_name = products[0][0]
cheapest_price = products[0][1]

most_expensive_name = products[0][0]
most_expensive_price = products[0][1]

for name, price in products:
    if price < cheapest_price:
        cheapest_price = price
        cheapest_name = name
    if price > most_expensive_price:
        most_expensive_price = price
        most_expensive_name = name

# Display results
print(f"Cheapest Product: {cheapest_name}, Price: {cheapest_price:.2f}")
print(f"Most Expensive Product: {most_expensive_name}, Price: {most_expensive_price:.2f}")
**Question 02**
# Get number from the user
num = int(input("Enter a number to calculate its factorial: "))

# Check for valid input
if num < 0:
    print("Factorial is not defined for negative numbers.")
else:
    factorial = 1
    for i in range(1, num + 1):
        factorial *= i
    print(f"The factorial of {num} is: {factorial}")
# Get number from the user
num = int(input("Enter a number to calculate its factorial: "))

# Check for valid input
if num < 0:
    print("Factorial is not defined for negative numbers.")
else:
    factorial = 1
    for i in range(1, num + 1):
        factorial *= i
    print(f"The factorial of {num} is: {factorial}")
    **Question 03**
    # List to store filenames
file_names = []

# Collect 5 filenames from the user
for i in range(5):
    file_name = input(f"Enter the name of file {i+1}: ")
    file_names.append(file_name)

# Count how many have the .py extension
py_count = 0
for name in file_names:
    if name.endswith(".py"):
        py_count += 1

# Display the result
print(f"\nNumber of files with .py extension: {py_count}")
