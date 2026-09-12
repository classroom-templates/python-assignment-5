# Assignment 5: Student Performance Report

## Description

In this assignment, you will design and implement a Python program that processes a fixed collection of student score records and produces a complete performance report.

Unlike the previous assignment, this program does **not** obtain data from the user. The complete data set is already available when the program begins.

The important change is that the program must now work with a **collection of related values**. The data must be retained, traversed, analyzed, and used to create additional information that is needed later in the program.

This assignment builds directly on the concepts from **Collections Part I** and the repetition material that came before it.

The primary programming concepts in this assignment include:

- lists;
- tuples;
- sequences;
- collection traversal;
- element access;
- mutability and immutability;
- constructing a new collection from an existing collection;
- counters and accumulators;
- running minimum and maximum values;
- preserving and reasoning about program state;
- systematic testing; and
- incremental software development.

The program specification defines the required behavior and output. You are responsible for designing the algorithm that produces that behavior.

## Learning Objectives

By completing this assignment, you should be able to:

- explain why a collection is preferable to a group of unrelated individual variables;
- traverse a collection and process each element;
- work with records containing multiple related values;
- access the individual values contained in a record;
- preserve the original collection while deriving new information from it;
- construct a new collection based on a condition;
- use counters and accumulators while traversing a collection;
- determine running minimum and maximum values without relying on arbitrary "magic" initial values;
- distinguish stored data from values calculated from that data;
- test collection-processing algorithms systematically;
- develop software incrementally using meaningful Git commits;
- use generative AI while retaining responsibility for design and verification; and
- create and maintain the complete project structure yourself.

## Background

Before beginning this assignment, you should have:

- completed **Assignment 1: Getting Started**;
- completed **Assignment 2: First Code**;
- completed **Assignment 3: Shipping Cost Calculator**;
- completed **Assignment 4: Score Analyzer**;
- completed the decision-making material;
- completed **Flow Control: Repetition Part I**;
- completed **Flow Control: Repetition Part II**;
- completed **Collections Part I**;
- reviewed the [Best Practices for Procedural Programming](https://katrompas.accprofessors.com/best-practice-procedural-programming);
- reviewed the course [Commenting Guidelines](https://katrompas.accprofessors.com/commenting);
- reviewed the [.gitignore guidelines](https://katrompas.accprofessors.com/gitignore-guidelines);
- reviewed the course [README Guidelines](https://katrompas.accprofessors.com/readme-guidelines); and
- reviewed the course [commit guidelines](https://katrompas.accprofessors.com/committing).

You are now expected to create and organize the executable portion of the project yourself.

## Starter Repository

Your starter repository contains only:

```text
ASSIGNMENT.md
ESSAY.md
```

No Python source file, README, or `.gitignore` is provided.

You are responsible for creating the remaining project files.

At minimum, your completed repository must contain:

```text
ASSIGNMENT.md
ESSAY.md
main.py
README.md
.gitignore
```

Create `main.py` using the standard course program structure with:

- a `main()` function; and
- the standard `if __name__ == "__main__":` entry-point guard.

You have used this structure in previous assignments and are now responsible for creating it correctly yourself.

## Required Data Collection

Your program must contain the following collection **exactly** as shown:

```python
students = [
    ("Alex", 88.5),
    ("Brianna", 94.0),
    ("Carlos", 67.5),
    ("Dina", 81.0),
    ("Evan", 59.5),
    ("Fatima", 73.0),
]
```

Each element of the list is one student record containing:

1. the student's name; and
2. the student's score.

Do not replace this collection with separate variables for each student.

Do not alter the order or values of the required collection in the final submitted program.

Your calculations must be performed from the collection at runtime. Do **not** hardcode calculated results such as the average, passing count, highest score, or names of passing students.

Your algorithm should continue to work correctly if the contents of the collection were changed while preserving the same general record structure.

## Program Requirements

Write a program that analyzes the required student collection and produces a performance report.

The program must:

1. begin by displaying exactly:

   ```text
   Student Performance Report
   ```

2. display the heading:

   ```text
   Student Scores
   ```

3. traverse the complete `students` collection and display every student and score in the original order;

4. calculate the total of all scores;

5. calculate the average score;

6. determine the student with the highest score;

7. determine the student with the lowest score;

8. count the number of passing and failing students;

9. construct and retain a **separate collection containing the names of all passing students**;

10. display the required summary; and

11. traverse the collection of passing student names and display those names in the original student order.

The program output must conform to the required interface described below.

## Displaying Student Scores

Display each student record in the original collection order using:

```text
<name>: <score>
```

Scores must display exactly two digits after the decimal point.

For example:

```text
Alex: 88.50
```

The complete student section must therefore display:

```text
Student Scores
Alex: 88.50
Brianna: 94.00
Carlos: 67.50
Dina: 81.00
Evan: 59.50
Fatima: 73.00
```

Review the final Classroom 50 autograding results and Feedback pull request.

Remember:The program must obtain these names and scores by traversing the collection.

Do not write six separate output statements containing the six student records.

## Passing and Failing

A score of **70 or greater** is passing.

A score below 70 is failing.

As the collection is processed, maintain the information necessary to report the total number of passing and failing students.

You must also create a separate collection containing the **names** of the passing students.

The contents of that collection must be produced by the program from the student records. Do not initialize it with the known passing names.

## Average

Calculate the arithmetic mean of all scores in the collection.

Display the result using exactly two digits after the decimal point:

```text
Average score: 77.25
```

The average must be calculated from the actual values in the collection.

## Highest and Lowest Scores

Determine the students with the highest and lowest scores.

Display:

```text
Highest score: Brianna - 94.00
Lowest score: Evan - 59.50
```

Do not initialize the highest or lowest score using an arbitrary large or small "magic number."

Your initialization should establish a valid starting state based on actual data.

For this assignment, the required collection will contain at least one student.

## Summary

After processing the complete collection, display:

```text
Summary
Students processed: 6
Average score: 77.25
Highest score: Brianna - 94.00
Lowest score: Evan - 59.50
Passing students: 4
Failing students: 2
```

`Students processed` must be derived from the collection rather than hardcoded.

## Passing Student Names

After the summary, display:

```text
Passing Student Names
Alex
Brianna
Dina
Fatima
```

These names must be produced by traversing the separate collection of passing student names created by your program.

Do not simply test the original `students` collection again and print passing names during the final section. The purpose of this requirement is to practice **constructing a new collection from an existing collection and then using that new collection later**.

## Complete Required Output

For the required data set, the completed program must produce:

```text
Student Performance Report
Student Scores
Alex: 88.50
Brianna: 94.00
Carlos: 67.50
Dina: 81.00
Evan: 59.50
Fatima: 73.00
Summary
Students processed: 6
Average score: 77.25
Highest score: Brianna - 94.00
Lowest score: Evan - 59.50
Passing students: 4
Failing students: 2
Passing Student Names
Alex
Brianna
Dina
Fatima
```

The required labels, capitalization, ordering, and numeric formatting are part of the program interface.

## Collection and Algorithm Standards

The purpose of this assignment is not merely to produce the expected text. It is to use collections appropriately.

Your program will be evaluated on whether:

- the supplied student collection is actually used as the source of the data;
- the collection is traversed rather than replaced with repetitive individual statements;
- the original student collection remains intact;
- calculated values are derived from the collection rather than hardcoded;
- the separate passing-student collection is constructed programmatically;
- the passing-student collection is actually used later;
- counters and accumulators are initialized and updated correctly;
- highest and lowest values are initialized from legitimate data;
- repetition clearly represents the work being performed; and
- the resulting program is readable, direct, and maintainable.

Remember:

> **Collections store related data. Repetition lets an algorithm operate over that data.**

The collection and the algorithm are different concepts, and both should be clear in your solution.

## Programming Constraints

Use programming concepts introduced in the course.

For this assignment, do **not** use:

- user input;
- additional user-defined functions beyond the required `main()` function;
- dictionaries;
- sets;
- NumPy;
- external libraries;
- file input/output;
- list comprehensions;
- generator expressions;
- `sum()`;
- `min()`;
- `max()`;
- `sorted()`;
- purposeful infinite loops such as `while True`;
- `break`; or
- `continue`.

The purpose of prohibiting the built-in aggregate functions in this assignment is to require you to practice traversal, accumulators, and running state explicitly.

Generative AI may suggest techniques outside the scope of this assignment. **Do not use unfamiliar or prohibited techniques** simply because AI generated them.

**You are responsible for understanding every part of the submitted program.**

## Code Quality

You will be evaluated on the readability, simplicity, structure, and quality of your code.

A program that merely reproduces the required output is not necessarily a correct solution to this assignment.

For example, this assignment is **not** satisfied by hardcoding the report because the output is already known.

Your code must actually process the supplied collection and calculate the results.

Use AI to help examine and improve your solution, but reject unnecessary complexity and techniques outside the course scope.

The [Best Practices for Procedural Programming](https://katrompas.accprofessors.com/best-practice-procedural-programming) apply.

## Development Process

Develop the program incrementally.

**Do not write the entire solution first and then commit the finished program.**

Your repository history must contain **at least eight meaningful student-created program-development commits** showing the program being developed incrementally.

Eight is the minimum, not the target.

A meaningful commit represents a coherent improvement to the working program.

You are responsible for:

- deciding appropriate development steps;
- testing your work before committing;
- writing clear, descriptive commit messages;
- pushing your work regularly;
- reviewing Classroom 50 feedback after pushes; and
- correcting problems as they are discovered.

Each meaningful commit must follow the course [commit guidelines](https://katrompas.accprofessors.com/committing).

Commits consisting only of formatting changes, arbitrary unfinished fragments, or changes made solely to increase the commit count are **not meaningful** development commits.

Changes made only to:

```text
README.md
ESSAY.md
.gitignore
```

do **not** count toward the eight required program-development commits.

Creating `main.py` and beginning the actual program may be part of a meaningful development commit if that commit represents a coherent working step.

## Generative AI

Use of generative AI is required as part of the development process.

You may use the generative AI system of your choice as a:

- tutor;
- programming partner;
- critic;
- debugging assistant;
- source of explanations;
- testing assistant; or
- aid in reasoning about collections and algorithms.

You may show the AI the complete assignment.

However, you are responsible for making the final engineering decisions.

In particular, you should be able to explain:

- why a collection is used;
- what each element of the supplied collection represents;
- how your traversal works;
- how program state changes during traversal;
- how the passing-student collection is constructed;
- how the minimum and maximum are determined; and
- how you verified that your calculated results are correct.

Your use and verification of AI will be documented in `ESSAY.md`.

## Testing

Testing is part of the development process even though this assignment has no user input.

Do not rely only on the fact that the final required data set produces the expected output.

During development, **temporarily test your algorithm with different collections** so that you know your program is calculating results rather than merely reproducing known answers.

Useful temporary test cases include:

- a collection containing only one student;
- a collection in which every student passes;
- a collection in which every student fails;
- a score of exactly `70`;
- a case in which the highest score appears first;
- a case in which the highest score appears last;
- a case in which the lowest score appears first;
- a case in which the lowest score appears last; and
- different score values that produce a different average.

After testing, restore the exact required `students` collection before submission.

Think about what each test is intended to demonstrate.

For this assignment, there are **NO autograder tests**. You are responsible for designing, running, and evaluating your own tests. Do not interpret the absence of automated tests as an absence of testing requirements.

## Code Documentation

Your program must follow the course [Commenting Guidelines](https://katrompas.accprofessors.com/commenting).

Because you create `main.py` yourself in this assignment, you are responsible for including:

- the required file comment header;
- the required function comment header for `main()`; and
- the standard `main()` entry-point structure.

Do not add comments that merely restate obvious individual lines of code.

Before submission, remove:

- debugging statements;
- commented-out code;
- temporary test data;
- temporary code; and
- unnecessary comments.

## `README.md`

Create `README.md` in the repository root.

Complete it according to the course [README Guidelines](https://katrompas.accprofessors.com/readme-guidelines).

The README must accurately document the program you actually submitted.

You are responsible for creating the complete Markdown structure yourself.

All Markdown files must be properly formatted and professional. Spelling, grammar, and writing quality count.

## `.gitignore`

Create an appropriate `.gitignore` file for this Python project.

Follow the course [.gitignore guidelines](https://katrompas.accprofessors.com/gitignore-guidelines).

The file must be present in the repository root before submission.

## `ESSAY.md`

Complete the supplied `ESSAY.md`.

The five questions will focus on:

- your use of generative AI;
- the structure and meaning of the student collection;
- how you traverse and process the collection;
- how and why you construct the separate passing-student collection; and
- how you tested and verified your collection-processing algorithm.

Each question is worth **2 points**, for a total of **10 points**.

Your answers must demonstrate **depth of thought and actual engagement with your work**. Short, vague, or trivial answers will not receive full credit.

Do not give answers such as:

> AI helped me solve problems.

or:

> I used a list because it worked.

Instead, explain **what you did, why you did it, and what you learned or verified**.

Whenever possible, include a **specific example from your program, your testing, or your interaction with AI**.

## Final Review and Submission

Before submitting the assignment, verify the complete repository.

### 1. Run the program

Run the program locally one final time:

```bash
python3 main.py
```

Depending on your system configuration, the command may instead be:

```bash
python main.py
```

Verify that the final output exactly matches the required output for the supplied data set.

### 2. Restore the required data

If you temporarily changed the student collection during testing, confirm that the exact required collection has been restored.

### 3. Check repository status

Run:

```bash
git status
```

Your working tree should be clean.

### 4. Review your development history

Run:

```bash
git log --oneline
```

Verify that your history contains at least eight meaningful program-development commits and that the history reflects incremental development.

### 5. Review the project structure

Confirm that the repository contains at least:

```text
ASSIGNMENT.md
ESSAY.md
main.py
README.md
.gitignore
```

### 6. Review GitHub

Open the repository on GitHub and confirm that:

- the final required student data is present;
- the final `main.py` is present;
- `README.md` is complete and properly rendered;
- `ESSAY.md` is complete and properly rendered;
- `.gitignore` is present; and
- all final changes have been pushed.

### 7. Submit through Blackboard

Copy the normal HTTPS URL for your GitHub repository and submit that URL in the Blackboard assignment.
