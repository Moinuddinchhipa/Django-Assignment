# Django-Assignment

Topic: Django Signals

Question 1: Are Django signals executed synchronously or asynchronously by default?
Django signals are executed synchronously by default. To demonstrate this, we use a post_save signal and introduce a delay. If the signal were asynchronous, it wouldn't block execution.

Question 2: Do Django signals run in the same thread as the caller?
Yes, Django signals run in the same thread as the caller. We can verify this by printing the thread ID inside both the signal and the caller function.

Question 3: Do Django signals run in the same database transaction as the caller?
Yes, Django signals run within the same database transaction as the caller. If a transaction is rolled back after a signal is executed, the changes will be reverted.

Topic: Custom Classes in Python
Task: Implement a Rectangle class with specific iteration behavior
class Rectangle:
    def __init__(self, length: int, width: int):
        self.length = length
        self.width = width

    def __iter__(self):
        yield {"length": self.length}
        yield {"width": self.width}

rectangle = Rectangle(10, 20)
for dimension in rectangle:
    print(dimension)

Expected Output:
     {'length': 10}
     {'width': 20}

How to Run the Code

Clone the repository and navigate to the project folder.
Install Django and set up a Django project if required.
Copy the provided code snippets into your Django app and test them.
Run the Python script for the Rectangle class to see the expected output.

