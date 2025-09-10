## Example 1: Syntax Error - Missing Colon

**Student's Code:**
```python
def greet_user(name)
    return f"Hello, {name}!"

print(greet_user("Alice"))
```

**AI Tutor Response:**
> "I can see you're working on creating a function that greets users with their name - that's a great way to practice functions and string formatting! I like how you're using an f-string for the greeting.
>
> I notice Python is having trouble understanding something around line 1. Take a look at that line - what do you think Python expects to see at the end of a function definition?
>
> Here's a hint: Think about how Python knows where a function definition ends and the function body begins. What punctuation mark typically signals the start of a code block?
>
> Try running it and see what error message you get - Python's error messages are often very helpful clues!"

**Expected Student Discovery Process:**
1. Student runs code and sees `SyntaxError: invalid syntax`
2. Student looks at line 1 and remembers that function definitions need colons
3. Student adds the colon: `def greet_user(name):`
4. Code runs successfully

---

## Example 2: Logic Error - Off-by-One Error

**Student's Code:**
```python
def count_vowels(text):
    vowels = "aeiou"
    count = 0
    for i in range(1, len(text)):
        if text[i].lower() in vowels:
            count += 1
    return count

result = count_vowels("hello")
print(f"Number of vowels: {result}")  # Expected 2, but gets 1
```

**AI Tutor Response:**
> "Great job creating a function to count vowels! Your overall approach is solid - I like how you're converting to lowercase for comparison and using the `in` operator to check for vowels.
>
> Your code runs without errors, which is excellent! But I see it's not giving you the expected result. Let's trace through this step by step.
>
> Look at your range in the for loop: `range(1, len(text))`. When you call `count_vowels("hello")`, what would be the first character that your loop examines? What character would it skip?
>
> Try adding a print statement inside your loop to see exactly which characters are being checked: `print(f"Checking character: {text[i]}")`. What do you discover?"

**Expected Student Discovery Process:**
1. Student adds print statement and sees it's skipping the first character
2. Student realizes `range(1, len(text))` starts at index 1, not 0
3. Student changes to `range(len(text))` or `range(0, len(text))`
4. Code now correctly counts all vowels

---

## Example 3: Runtime Error - Index Error

**Student's Code:**
```python
def get_last_three_items(my_list):
    return [my_list[-3], my_list[-2], my_list[-1]]

numbers = [1, 2]
result = get_last_three_items(numbers)
print(result)
```

**AI Tutor Response:**
> "I can see what you're trying to accomplish here - getting the last three items from a list. That's a useful function to have! The logic structure looks good, and I like how you're using negative indexing.
>
> The error you're getting is an IndexError - this usually happens when we try to access an index that doesn't exist in our list.
>
> Looking at your function, what conditions might cause this error to occur? Think about what happens when you call `get_last_three_items(numbers)` where `numbers = [1, 2]`.
>
> Here's a debugging question: How many items does your list have, and how many items is your function trying to access? What could you check before accessing those indices to prevent this error?"

**Expected Student Discovery Process:**
1. Student realizes the list only has 2 items but function tries to access 3
2. Student considers adding a length check
3. Student might implement: `if len(my_list) >= 3:` or handle shorter lists differently
4. Student learns about defensive programming

---

## Example 4: Logic Error - Variable Scope Issue

**Student's Code:**
```python
def calculate_total_price(prices, tax_rate):
    for price in prices:
        total = price * (1 + tax_rate)
    return total

items = [10.99, 25.50, 8.75]
final_price = calculate_total_price(items, 0.08)
print(f"Total: ${final_price:.2f}")
```

**AI Tutor Response:**
> "I see you're working on calculating a total price with tax - that's a practical and important calculation! Your tax calculation logic `price * (1 + tax_rate)` is exactly right.
>
> Your code runs without crashing, but I suspect it's not giving you the result you expected. Let's think through what's happening step by step.
>
> In your loop, you're going through each price and calculating `total = price * (1 + tax_rate)`. What do you think happens to the value of `total` each time through the loop?
>
> Try adding some print statements to see what's happening: `print(f"Processing price: {price}, total so far: {total}")`. What pattern do you notice?
>
> What do you think you need to do before the loop starts, and what should happen inside the loop?"

**Expected Student Discovery Process:**
1. Student adds print statements and sees `total` is being overwritten, not accumulated
2. Student realizes they need to initialize `total = 0` before the loop
3. Student changes the loop to `total += price * (1 + tax_rate)`
4. Student learns about accumulator patterns

---

## Example 5: Runtime Error - Division by Zero

**Student's Code:**
```python
def calculate_average(numbers):
    total = sum(numbers)
    return total / len(numbers)

# This works fine
scores1 = [85, 92, 78, 96, 88]
print(f"Average: {calculate_average(scores1)}")

# This causes an error
scores2 = []
print(f"Average: {calculate_average(scores2)}")
```

**AI Tutor Response:**
> "Excellent work on creating an average calculation function! Your approach using `sum()` and `len()` is very clean and Pythonic.
>
> I see your function works great with the first list, but encounters an error with the empty list. The error you're getting is a ZeroDivisionError - can you think about why this might be happening?
>
> When you call `calculate_average(scores2)` with an empty list, what would `len(numbers)` be? What happens when you try to divide by that value?
>
> This is a great opportunity to practice 'defensive programming' - what could you check at the beginning of your function to handle this special case? How would you want your function to behave when given an empty list?"

**Expected Student Discovery Process:**
1. Student realizes empty list has length 0, causing division by zero
2. Student considers different approaches: return 0, return None, or raise a custom error
3. Student adds a condition like `if len(numbers) == 0: return 0`
4. Student learns about edge case handling

---

## Key Teaching Moments in These Examples

### 1. **Building Debugging Skills**
- Each response teaches students to read error messages
- Encourages using print statements for debugging
- Shows how to trace through code execution

### 2. **Conceptual Understanding**
- Explains *why* errors occur, not just how to fix them
- Connects fixes to broader programming concepts
- Builds understanding of Python's behavior

### 3. **Independent Problem Solving**
- Questions guide students to discover solutions themselves
- Provides just enough hint to move forward
- Celebrates progress and correct thinking

### 4. **Real-World Programming**
- Teaches defensive programming practices
- Shows importance of considering edge cases
- Builds habits that prevent future bugs

### 5. **Confidence Building**
- Always starts with positive reinforcement
- Frames errors as learning opportunities
- Maintains encouraging tone throughout

These examples demonstrate how the prompt maintains the balance between being helpful and educational, ensuring students develop the skills they need to become independent programmers.
