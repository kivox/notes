---
{"dg-publish":true,"permalink":"/computer-science/mastermind/mastermind/","dgHomeLink":true,"dgPassFrontmatter":false}
---

# Mastermind

>Mastermind Generate a random 4 digit number. The player has to keep inputting 4 digit numbers until they guess the randomly generated number. After each unsuccessful try it will say how many numbers they got correct, but not which position they got right. At the end of the game it will congratulate the user and say how many tries it took.

![[Flowchart.png|Flowchart.png]]

## Thought process
- Generate number
```python
rand_num = random.randrange(1000, 10000)
```

- Turn number into string
```python
rand_str = str(rand_num)
```

- Get user to input string
```python
guess = input("Guess a 4 digit number (x > 1000 && x < 10000)")
```

- Check if user is correct, if correct return "You win!" and exit.
```python
if guess == rand_str:
	print("You win")
```

- For each number in user's guess, check if random number contains it
```python
correct = 0
for i in range(0, 4):
	if (guess[i] == rand_str[i]):
		correct += 1
```
- Let the user know how many numbers they got correct.
```python
print(f"You got the number wrong, you got {correct} digits correct")
```
- Loop


## Bringing it all together
```python
import random

# generate a random number
rand_str = str(random.randrange(1000, 10000))

# initate tries counter
tries = 0

# start loop
while True:
	# let the user guess
	guess = input("Guess a 4 digit number (x > 1000 && x < 10000): ")

	# validation, wether a number is 4 digits
	if len(guess) < 4 or len(guess) <= 0:
	  print("Your guess must be 4 digits")
	  continue

	# increment tries counter
	tries += 1

	# check if answer is correct
	if guess == rand_str:
		print("You guessed correct!")
		break

	# count how many digits were correct in the user's guess
	correct = 0
	for i in range(0, 4):
		if (guess[i] == rand_str[i]):
			correct += 1

	# inform the user of how successful they were
	if correct > 0:
		print(f"You didn't quite get it, but you got {correct} correct")
	else:
		print(f"Try again!")
```