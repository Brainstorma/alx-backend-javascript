# 0x04. Typescript

This project is part of the Holberton School curriculum. It introduces the basics of Typescript, a superset of JavaScript that adds static types and other features.

## Learning Objectives

- Basic types in Typescript
- Interfaces, Classes, and functions
- How to work with the tsc command line
- How to use namespaces and modules
- How to merge declaration files
- How to use an ambient Namespace to import an external library
- Basic nominal typing with Typescript

## Tasks

### 0. Creating an interface for a student

Create an interface named `Student` that defines the following properties:

- `firstName` (string)
- `lastName` (string)
- `age` (number)
- `location` (string)

Create an array named `studentsList` where each item is a `Student` object.

Create a function named `renderStudent` that takes a `Student` object as an argument and returns an HTML element (`<li>`) that displays the student's full name and location.

Use the function to render each student in the array and append them to the `<ul>` element in the document with the id `list`.

[Link to task](./task_0/js/main.ts)

### 1. Let's build a Teacher interface

Create an interface named `Teacher` that defines the following properties:

- `firstName` (string, readonly)
- `lastName` (string, readonly)
- `fullTimeEmployee` (boolean)
- `location` (string)
- `yearsOfExperience` (number, optional)
- `[propName: string]: any;`

Create another interface named `Directors` that extends from `Teacher` and adds a property named `numberOfReports` (number).

Create two objects, one for a teacher and one for a director, using their respective interfaces.

Create a function named `printTeacher` that takes two arguments: `firstName` (string) and `lastName` (string). The function should return the first letter of the first name and the full last name separated by a dot (`.`). For example: printTeacher("John", "Doe") => "J.Doe".

[Link to task](./task_1/js/main.ts)

### 2. Extending the Teacher class

Create an interface named `classInterface` that defines the following properties:

- `firstName` (string)
- `lastName` (string)
- `workOnHomework()` (function that returns a string)
- `displayName()` (function that returns a string)

Create another interface named `classConstructor` that defines how to create a new instance of `classInterface`. It should take two arguments: `firstName` (string) and `lastName` (string).

Create a class named `StudentClass` that implements both interfaces. The constructor should assign the arguments to the corresponding properties. The methods should return `"Currently working"` and the first name respectively.

Create an instance of the class and test its methods.

[Link to task](./task_2/js/main.ts)

### 3. Initialize variables

Create variables named:

- `firstName`: type string, value "Holberton"
- `lastName`: type string, value "School"
- `age`: type number, value 98
- `job`: type string, value "Software Engineer"
- `points`: type number, value 100
- `rating`: type number or string, value 80

[Link to task](./task_3/js/main.ts)

### 4. Create functions specific to employees

Create two types: one named `Subject`, which is an enum with values `"Math"`, `"History"`, `"English"`, `"Spanish"`, `"French"`; and another named `Teacher`, which is an object with two properties: `"subject"` of type Subject and `"yearsOfExperience"` of type number.

Create two functions: one named `teachClass`, which takes a Teacher object as an argument and returns a string in the format `"Today we are learning about {subject}"`; and another named `welcomeTeacher`, which takes a Teacher object as an argument and returns a string in the format `"Welcome {subject} teacher!"`.

Create two objects, one for a Math teacher and one for a History teacher, using the Teacher type.

Use the functions to print the messages for each teacher.

[Link to task](./task_4/js/main.ts)

### 5. Creating generic functions

Create a generic function named `createTuple` that takes two arguments of any type and returns an array of those types.

Create another generic function named `createTuple2` that takes three arguments of any type and returns an array of those types.

Use the functions to create tuples of different types and lengths.

[Link to task](./task_5/js/main.ts)

### 6. Write a namespace

Create a namespace named `Subjects` that contains the following:

- An interface named `Teacher` that defines a property named `experienceTeachingJava` of type number.
- A class named `Java` that implements the interface `Subject` from task 4. It should have a constructor that takes one argument: `teacher` of type Teacher. It should also override the method `getRequirements()` to return `"Java is important"` and the method `getAvailableTeacher()` to return `"Available teacher: {teacher.firstName}"` if the teacher's experience is greater than zero, or `"No available teacher"` otherwise.
- A class named `Cpp` that implements the interface `Subject` from task 4. It should have a constructor that takes one argument: `teacher` of type Teacher. It should also override the method `getRequirements()` to return `"C++ is important"` and the method `getAvailableTeacher()` to return `"Available teacher: {teacher.firstName}"` if the teacher's experience is greater than zero, or `"No available teacher"` otherwise.

[Link to task](./task_6/js/main.ts)

### 7. Write another namespace

Create another namespace named `Subjects` that contains the following:

- An interface named `Teacher` that defines a property named `experienceTeachingReact` of type number.
- A class named `React` that implements the interface `Subject` from task 4. It should have a constructor that takes one argument: `teacher` of type Teacher. It should also override the method `getRequirements()` to return `"React is important"` and the method `getAvailableTeacher()` to return `"Available teacher: {teacher.firstName}"` if the teacher's experience is greater than zero, or `"No available teacher"` otherwise.

Use declaration merging to append these definitions to the ones from task 6.

[Link to task](./task_7/js/main.ts)

### 8. Ambient Namespaces

Create an ambient namespace named `Subjects` that contains the following:

- An interface named `Student` that defines two properties: `firstName` of type string and `lastName` of type string.
- A function named `studentAverages` that takes an array of Student objects as an argument and returns an array of numbers representing their average grades.

Use triple-slash directives to import this namespace from another file.

[Link to task](./task_8/js/main.ts)

### 9. Namespace & Declaration merging

Create an ambient namespace named `Subjects` that contains the following:

- An interface named `Teacher` that defines two properties: `firstName` of type string and `lastName` of type string.
- A function named `printTeacher` that takes a Teacher object as an argument and returns a string in the format `{firstLetterOfFirstName}. {lastName}`.

Use declaration merging to append these definitions to the ones from task 8.

[Link to task](./task_9/js/main.ts)

### 10. Update task_4/js/main.ts

Update the file from task 4 by adding triple-slash directives to import the ambient namespaces from tasks 8 and 9.

Use the imported namespaces to create objects and call functions.

[Link to task](./task_10/js/main.ts)

### 11. Brand convention & Nominal typing

Create two types: one named `Brand`,

## Tasks To Complete

+ [x] 0. **Creating an interface for a student**<br/>[task_0/js/main.ts](task_0/js/main.ts) contains a script that meets the following requirements:
  + Write an interface named `Student` that accepts the following elements: `firstName(string)`, `lastName(string)`, `age(number)`, and `location(string)`.
  + Create two students, and create an array named `studentsList` containing the two variables.
  + Using Vanilla Javascript, render a table and for each elements in the array, append a new row to the table.
  + Each row should contain the first name of the student and the location.
  + When running, Webpack should return `No type errors found`.
  + Every variable should use TypeScript when possible.

+ [x] 1. **Let's build a Teacher interface**<br/>[task_1/js/main.ts](task_1/js/main.ts) contains a script that meets the following requirements:
  + `firstName(string)` and `lastName(string)`. These two attributes should only be modifiable when a Teacher is first initialized.
  + `fullTimeEmployee(boolean)` this attribute should always be defined.
  + `yearsOfExperience(number)` this attribute is optional.
  + `location(string)` this attribute should always be defined.
  + Add the possibility to add any attribute to the Object like `contract(boolean)` without specifying the name of the attribute.

+ [x] 2. **Extending the Teacher class**<br/>[task_1/js/main.ts](task_1/js/main.ts) contains the following updates:
  + Write an interface named `Directors` that extends `Teacher`. It requires an attribute named `numberOfReports(number)`.

+ [x] 3. **Printing teachers**<br/>[task_1/js/main.ts](task_1/js/main.ts) contains the following updates:
  + Write a function `printTeacher`:
    + It accepts two arguments `firstName` and `lastName`.
    + It returns the first letter of the `firstName` and the full `lastName`.
    + Example: `printTeacher("John", "Doe") -> J. Doe`.
  + Write an interface for the function named `printTeacherFunction`.

+ [x] 4. **Writing a class**<br/>[task_1/js/main.ts](task_1/js/main.ts) contains the following updates:
  + Write a Class named `StudentClass`:
    + The constructor accepts `firstName(string)` and `lastName(string)` arguments.
    + The class has a method named `workOnHomework` that return the string `Currently working`.
    + The class has a method named `displayName`. It returns the firstName of the student.
    + The constructor of the class should be described through an Interface.
    + The class should be described through an Interface.
    + When running `npm run build`, no TypeScript error should be displayed.
    + Every variable should use TypeScript when possible.

+ [x] 5. **Advanced types Part 1**<br/>[task_2/js/main.ts](task_2/js/main.ts) contains a script that meets the following requirements:
  + Create the `DirectorInterface` interface with the 3 expected methods:
    + `workFromHome()` returning a string.
    + `getCoffeeBreak()` returning a string.
    + `workDirectorTasks()` returning a string.
  + Create the `TeacherInterface` interface with the 3 expected methods:
    + `workFromHome()` returning a string.
    + `getCoffeeBreak()` returning a string.
    + `workTeacherTasks()` returning a string.
  + Create a class `Director` that will implement `DirectorInterface`:
    + `workFromHome` should return the string `Working from home`.
    + `getToWork` should return the string `Getting a coffee break`.
    + `workDirectorTasks` should return the string `Getting to director tasks`.
  + Create a class `Teacher` that will implement `TeacherInterface`:
    + `workFromHome` should return the string `Cannot work from home`.
    + `getCoffeeBreak` should return the string `Cannot have a break`.
    + `workTeacherTasks` should return the string `Getting to work`.
  + Create a function `createEmployee` with the following requirements:
    + It can return either a `Director` or a `Teacher` instance.
    + It accepts 1 arguments:
      + `salary`(either number or string).
    + If `salary` is a number and less than 500 - It should return a new `Teacher`. Otherwise it should return a `Director`.

+ [x] 6. **Creating functions specific to employees**<br/>[task_2/js/main.ts](task_2/js/main.ts) contains the following updates:
  + Write a function `isDirector`:
    + It accepts `employee` as an argument.
    + It will be used as a type predicate and if the employee is a director.
  + Write a function `executeWork`:
    + It accepts `employee` as an argument.
    + If the employee is a `Director`, it will call `workDirectorTasks`.
    + If the employee is a `Teacher`, it will call `workTeacherTasks`.

+ [x] 7. **String literal types**<br/>[task_2/js/main.ts](task_2/js/main.ts) contains the following updates:
  + Write a String literal type named `Subjects` that allows a variable to have the value `Math` or `History` only.
  + Write a function named `teachClass`:
    + It takes `todayClass` as an argument.
    + It will return the string `Teaching Math` if `todayClass` is `Math`.
    + It will return the string `Teaching History` if `todayClass` is `History`.

+ [x] 8. **Ambient Namespaces**
  + [task_3/js/interfaces.ts](task_3/js/interfaces.ts) contains a script that meets the following requirements:
    + Export a type `RowID` and set it equal to `number`.
    + Export an interface `RowElement` that contains these 3 fields:
      + `firstName`: `string`.
      + `lastName`: `string`.
      + `age?`: `number`.
  + You are building the next part of the application architecture. The goal is to save the entities to a database. Because of time constraints, you can't write a connector to the database, and you decided to download a library called `crud.js`. Copy the file, which is shown below, into the [task_3/js](task_3/js) directory.
    ```js
    export function insertRow(row) {
      console.log('Insert row', row);
      return Math.floor(Math.random() * Math.floor(1000));
    }

    export function deleteRow(rowId) {
      console.log('Delete row id', rowId);
      return;
    }

    export function updateRow(rowId, row) {
      console.log(`Update row ${rowId}`, row);

      return rowId;
    }
    ```
  + [task_3/js/crud.d.ts](task_3/js/crud.d.ts) is an ambient file that meets the following requirements:
    + Export the type declarations for each crud function.
    + At the top of the file, import `RowID` and `RowElement` from [task_3/js/interfaces.ts](task_3/js/interfaces.ts).
  + [task_3/js/main.ts](task_3/js/main.ts) contains a script that meets the following requirements:
    + At the top of the file create a [triple slash directive](https://www.typescriptlang.org/docs/handbook/triple-slash-directives.html) that includes all the dependencies from [task_3/js/crud.d.ts](task_3/js/crud.d.ts).
    + Import the `RowID` type and `RowElement` from [task_3/js/interfaces.ts](task_3/js/interfaces.ts).
    + Import everything from [task_3/js/crud.js](task_3/js/crud.js) as `CRUD`.
    + Create an object called `row` with the type `RowElement` with the fields set to these values:
      + `firstName`: `Guillaume`.
      + `lastName`: `Salva`.
    + Create a `const` variable named `newRowID` with the type `RowID` and assign it the value of the `insertRow` command.
    + Next, create a `const` variable named `updatedRow` with the type `RowElement` and update `row` with an age field set to `23`.
    + Finally, call the `updateRow` and `deleteRow` commands.

+ [x] 9. **Namespace & Declaration merging**
  + [task_4/js/subjects/Teacher.ts](task_4/js/subjects/Teacher.ts) contains a script that meets the following requirements:
    + Export a `Teacher` interface in a namespace named `Subjects`.
    + The interface requires `firstName` and `lastName` as string.
  + [task_4/js/subjects/Subject.ts](task_4/js/subjects/Subject.ts) contains a script that meets the following requirements:
    + Export a `Subject` class in a namespace named `Subjects`.
    + The class has one attribute `teacher` that implements the `Teacher` interface.
    + the class has one setter method `setTeacher` that accepts a `teacher` in argument (and as setter, set the instance attribute `teacher` with it).
  + [task_4/js/subjects/Cpp.ts](task_4/js/subjects/Cpp.ts) contains a script that meets the following requirements:
    + Using declaration merging, add a new optional attribute `experienceTeachingC` (number) to the `Teacher` interface in a namespace named `Subjects`.
    + Export a class `Cpp` extending from `Subject` in a namespace named `Subjects`.
      + Write a method named `getRequirements` that will return a string `Here is the list of requirements for Cpp`.
      + Write a method named `getAvailableTeacher` that will return a string `Available Teacher: <first name of teacher>`.
      + If the teacher doesn't have any experience in teaching C, then the method should return a string `No available teacher`.
  + [task_4/js/subjects/React.ts](task_4/js/subjects/React.ts) contains a script that meets the following requirements:
    + Export a `React` class in a namespace named `Subjects`.
    + Add a new attribute `experienceTeachingReact?` (number) to the `Teacher` interface.
    + In the class, write a method named `getRequirements` that will return a string `Here is the list of requirements for React`.
    + Write a method named `getAvailableTeacher` that will return a string `Available Teacher: <first name of teacher>`.
    + If the teacher doesn't have any experience in teaching React, then the method should return a string `No available teacher`.
  + [task_4/js/subjects/Java.ts](task_4/js/subjects/Java.ts) contains a script that meets the following requirements:
    + Export a `Java` class in a namespace named `Subjects`.
    + Add a new attribute `experienceTeachingJava?` (number) to the `Teacher` interface.
    + In the class, write a method named `getRequirements` that will return a string `Here is the list of requirements for Java`.
    + Write a method named `getAvailableTeacher` that will return a string `Available Teacher: <first name of teacher>`.
    + If the teacher doesn't have any experience in teaching Java, then the method should return a string `No available teacher`.

+ [x] 10. **Update task_4/js/main.ts**<br/>[task_4/js/main.ts](task_4/js/main.ts) contains the following updates:
  + Create and export a constant `cpp` for Cpp Subjects.
  + Create and export a constant `java` for Java Subjects.
  + Create and export a constant `react` for React Subjects.
  + Create and export one Teacher object `cTeacher` with `experienceTeachingC = 10`.
  + For Cpp subject, log to the console `C++`, set `cTeacher` as the teacher, call the two methods `getRequirements` and `getAvailableTeacher` and print the strings they return.
  + For Java subject, log to the console `Java`, set `cTeacher` as the teacher, call the two methods `getRequirements` and `getAvailableTeacher`, and print the strings they return.
  + For React subject, log to the console `React`, set `cTeacher` as the teacher, call the two methods `getRequirements` and `getAvailableTeacher`, and print the strings they return.

+ [x] 11. **Brand convention & Nominal typing**<br/>[task_5/js/main.ts](task_5/js/main.ts) contains a script that meets the following requirements:
  + Create two interfaces `MajorCredits` and `MinorCredits`:
    + Each interface defines a number named `credits`.
    + Add a brand property to each interface in order to uniquely identify each of them.
  + Create two functions named `sumMajorCredits` and `sumMinorCredits`:
    + Each function takes two arguments `subject1` and `subject2`.
    + `sumMajorCredits` returns `MajorCredits` value and `sumMinorCredits` returns `MinorCredits` value.
    + Each function sums the credits of the two subjects.

