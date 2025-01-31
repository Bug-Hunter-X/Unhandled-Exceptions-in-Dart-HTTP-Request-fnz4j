# Unhandled Exceptions in Dart HTTP Request

This repository demonstrates a common error in Dart applications: insufficient error handling in asynchronous operations, specifically HTTP requests.

The `bug.dart` file contains code that fetches data from an API. However, it lacks robust error handling, potentially leading to crashes or unexpected behavior.

The `bugSolution.dart` file provides a corrected version with improved error handling. It addresses potential exceptions during the API call, JSON decoding, and other unexpected scenarios.

## How to reproduce the bug:

1.  Run `bug.dart`.
2.  Observe that there is no proper handling of potential errors, such as a network error or a non-200 status code from the API.

## Solution:

The improved version in `bugSolution.dart` incorporates comprehensive error handling using `try-catch` blocks and checks the HTTP status code before processing the response.  It also utilizes the `rethrow` keyword to allow for error handling at different levels of the call stack.