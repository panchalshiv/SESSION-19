[session_19_README.md](https://github.com/user-attachments/files/32117518/session_19_README.md)
# Session 19 – Python OOP Basics (Classes & Objects)

This notebook contains a set of small Python exercises introducing Object-Oriented Programming concepts — classes, objects, attributes, and methods — using music streaming (Spotify-style) and food delivery (Zomato-style) examples.

## Contents

### 1. Basic Class with Attributes
Defines a `Song` class with `title`, `artist`, and `duration` attributes, and creates an object to access them directly.

```python
class Song:
    def __init__(self, title, artist, duration):
        self.title = title
        self.artist = artist
        self.duration = duration
```

**Output:**
```
Tum Hi Ho
Arijit Singh
262
```

### 2. Accessing Object Attributes
Same `Song` class, demonstrating attribute access with labeled print statements for a "favorite Spotify song" example.

**Output:**
```
Title: Tum Hi Ho
Artist: Arijit Singh
```

### 3. Adding a Method
Extends the `Song` class with a `play_preview()` method that prints a formatted preview message using the object's own attributes.

```python
def play_preview(self):
    print(f"Playing 30-second preview of {self.title} by {self.artist}")
```

**Output:** `Playing 30-second preview of Tum Hi Ho by Arijit Singh`

### 4. Class with a List Attribute and Running Total
Defines a `FoodOrder` class that tracks a restaurant name, a list of ordered items, and a running total price. The `add_item()` method appends an item and updates the total.

```python
class FoodOrder:
    def __init__(self, restaurant_name):
        self.restaurant_name = restaurant_name
        self.items = []
        self.total_price = 0

    def add_item(self, item, price):
        self.items.append(item)
        self.total_price += price
```

**Output:**
```
Restaurant: Zomato Restaurant
Items: ['Pizza', 'Burger']
Total Price: 448
```

### 5. Tracking State with a Counter
Extends `Song` with a `play_count` attribute initialized to `0`, and an `increment_play_count()` method to track how many times a song has been played.

```python
def increment_play_count(self):
    self.play_count += 1
```

**Output:**
```
Song: Tum Hi Ho
Play Count: 3
```

## Concepts Covered
- Defining a class with `__init__`
- Instance attributes vs. instance methods
- Creating and using objects
- Mutating object state via method calls (lists, running totals, counters)

## Requirements
- Python 3.x
- Standard library only

## Notes
The notebook includes several empty cells at the end, likely reserved for additional exercises or practice.
