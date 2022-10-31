---
{"dg-publish":true,"permalink":"/computer-science/challenges/luhn/","dgHomeLink":true,"dgPassFrontmatter":false}
---


# Luhn Algorithm
>Takes in a credit card number from a common credit card vendor (Visa, MasterCard, American Express, Discoverer) and validates it to make sure that it is a valid number.
```python
# The Luhn algorithm starts by the end of the number, from the last right digit to the first left digit.  
# Multiplying by 2 all digits of even rank.  
# If the double of a digit is equal or superior to 10, replace it by the sum of its digits.  
# Realize the sum  
  
def double(n):  
    digit = n * 2  
    if digit > 9:  
        return digit - 9  
    else:  
        return digit  
  
  
cc = ""  
while True:  
    cc = input("Please enter the card number: ")  
    if not cc.isnumeric():  
        print("The card number provided is invalid (non-numeric input)")  
        continue  
    else:  
        # convert string to number, then back to string  
        # this is done to remove spaces and other inconsistencies as we want just the card number        number = str(int(cc))  
        break  
  
total = 0  
if 11 < len(cc) < 17:  
    for num in range(2, len(cc) + 1):  
        if num % 2:  
            total += int(cc[num * -1])  
        else:  
            total += double(int(cc[num * -1]))  
  
    if (total * 9) % 10 != int(cc[-1]):  
        print("The card number provided is invalid")  
    else:  
        print("The card number provided is valid")  
else:  
    print("The card number provided is invalid")
```

