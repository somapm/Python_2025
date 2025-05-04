Exercise01
price = "15.0"
code = "007"
name = "Alice"
is_active = True

#print(int(price))             # ValueError: invalid literal for int() with base 10: '15.0'

print(int(code))

# print(int(name))            # ValueError : could not convert string to int: 'Alice', # دلیل: رشته حاوی کاراکترهای غیرعددی است.

print(int(is_active))
score="3.14"
print(float(score))

amount='3,14'
#print(float(amount)) # ValueError: could not convert string to float: '3,14'


value="NaN"
print(float(value)) # رشته "NaN" (یا حتی "nan") در پایتون تبدیل می‌شه به float('nan') که معادل "Not a Number" هست. هنوز float محسوب می‌شه ولی خاصه—به‌درد کارهای عددی معمول نمی‌خوره.



is_logged_in=False
print(float(is_logged_in))
float("NaN") == float("NaN")  # نتیجه: False
# چون nan هیچ‌وقت با خودش برابر نیست!
age=12
print(str(age))

average_score=17.5
print(str(average_score))

is_verified=True
print(str(is_verified))

username=""
print(bool(username))

status='False'
print(bool(status))

comment=" "
print(bool(comment))


visits=0
print(bool(visits))
# Step 1: Define a string that looks like a float
price_str = '120.5'
# price_str is a string, not a number yet

# Step 2: Convert string to float, then to int
price = int(float(price_str))
# float('120.5') -> 120.5
# int(120.5) -> 120 (removes decimal part)

print('price =', price)
# Output: price = 120

# Step 3: Convert the integer price back to string and concatenate '0'
code = str(price) + '0'
# str(120) -> '120'
# '120' + '0' -> '1200' (still a string)

print('code =', code)
# Output: code = 1200

# Step 4: Concatenate code (a string) with price_str (also a string)
result = code + price_str
# '1200' + '120.5' -> '1200120.5'

print('result =', result)
# Output: result = 1200120.5

# Step 5: Convert the result string into a float
final_price = float(result)
# float('1200120.5') -> 1200120.5

print('final_price =', final_price)
# Output: final_price = 1200120.5

# Step 6: Try to convert final_price to int and assign to discounted
# ⚠️ There's a typo here: `final_price_` (with underscore) is not defined
# So this line will raise a NameError
# discounted = int(final_price_)

# ✅ Correct version:
discounted = int(final_price)
# int(1200120.5) -> 1200120

print('discounted =', discounted)
# Output: discounted = 1200120
# Get input from the user
num1 = input("Enter the first number: ")
num2 = input("Enter the second number: ")

# Convert the inputs to float (or int if you prefer)
num1 = float(num1)
num2 = float(num2)

# Compare and print the result
print(num1 == num2)
# Initial values
a = input("Enter value for a: ")
b = input("Enter value for b: ")

# Print before swapping
print("Before swapping:")
print("a =", a)
print("b =", b)

# Swap the values
a, b = b, a

# Print after swapping
print("After swapping:")
print("a =", a)
print("b =", b)
# Multiple assignment – This is valid
price1, price2, price3 = 100, 200, 30.5
# ✅ This assigns 100 to price1, 200 to price2, and 30.5 to price3

# Chain assignment – Also valid
score1 = score2 = 18.9
# ✅ This assigns 18.9 to both score1 and score2

# Tuple unpacking – ❌ This will raise an error
# str1, str2, str3 = 'python', 'java'
# ❌ ValueError: not enough values to unpack (expected 3, got 2)

# ✅ Fixed version (add a third value):
str1, str2, str3 = 'python', 'java', 'c++'
# ✅ Now each variable gets one string
price1, price2, price3 = 100, 200, 30.5
print(price1, price2, price3)  # Output: 100 200 30.5

score1 = score2 = 18.9
print(score1, score2)          # Output: 18.9 18.9

str1, str2, str3 = 'python', 'java', 'c++'
print(str1, str2, str3)        # Output: python java c++
Exercise02
# Take input from the user
user_input = input("Enter a string: ")

# Get the length of the string
length = len(user_input)

# Display the first, middle, and last character
first_char = user_input[0]
last_char = user_input[-1]
middle_char = user_input[length // 2]

print("First character:", first_char)
print("Middle character:", middle_char)
print("Last character:", last_char)

# Display the length of the string
print("Length of the string:", length)

# Display characters at even indexes (0, 2, 4, ...)
even_index_chars = user_input[::2]
print("Characters at even indexes:", even_index_chars)

# Display the string in reverse
reversed_string = user_input[::-1]
print("Reversed string:", reversed_string)

# Display the first half and second half of the string
half = length // 2
first_half = user_input[:half]
second_half = user_input[half:]
print("First half of the string:", first_half)
print("Second half of the string:", second_half)
# Take student ID as input
student_id = input("Enter your student ID: ")

# Check if the input contains only digits
is_numeric = student_id.isdigit()

# Display the result
print(is_numeric)
# دریافت ورودی از کاربر
student_id = input("Enter your student ID: ")

# فرض می‌کنیم اول درست است
only_digits = True

# بررسی تک‌تک کاراکترها
for char in student_id:
    if char < '0' or char > '9':
        only_digits = False
        break

# چاپ نتیجه
if only_digits:
    print(True)
else:
    print(False)
# دریافت ورودی از کاربر
student_id = input("Enter your student ID: ")

# فرض می‌کنیم اول درست است
only_digits = True

# بررسی تک‌تک کاراکترها
for char in student_id:
    if char < '0' or char > '9':
        only_digits = False
        break

# چاپ نتیجه
if only_digits:
    print(True)
else:
    print(False)
# دریافت ورودی از کاربر
student_id = input("Enter your student ID: ")

# فرض می‌کنیم اول درست است
only_digits = True

# بررسی تک‌تک کاراکترها
for char in student_id:
    if char < '0' or char > '9':
        only_digits = False
        break

# چاپ نتیجه
if only_digits:
    print(True)
else:
    print(False)
# Take input from the user
user_input = input("Enter a string: ")

# Remove all spaces (including spaces in the middle)
no_spaces = ""
for char in user_input:
    if char != " ":
        no_spaces += char

# Display the result
print("String without spaces:", no_spaces)
code = "42"
padded = code.zfill(5)
print(padded)
text = "name:Alice"
result = text.partition(":")
print(result)
