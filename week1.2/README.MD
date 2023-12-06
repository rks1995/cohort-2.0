# Why Languages?

- Developers build applications using languages (c, c++, java, javascript)
- Developers write high level code in these languages
- Every languages has its own **compiler** which converts languages to zero's and one's (01)

# Interpreted v/s Compiled language

| Compiled Language | Interpreted Language |
| :-- | :-- |
| - Compiled languages are languages where developers write high level code make the code to binary(after complied) and finally executes the binary.| - Interpreted languages are languages where converting high level code to binary is not required. Usually go line by line. |
| - Usually don't compiled if there is error in the code | Can run partially if error comes later |
| -  Example c++, Java | - Example javascript, python

# Static v/s Dynamic languages


| Static Language | Dynamic Language |
| :-- | :-- |
| - Variable type is known in compiled time.| - Its a loosely typed language, means the type is associated in run time. |
| - All kinds of types is check by the compiler | Developers can write faster code as they do not need to specify the types |
| -  Example c++, Java | - Example javascript, python

# Single threaded nature of JS

- Single threaded means only one process can be executed by a single threaded machine.
- single threaded nature of js **doesn't allow code splitting into two separate process**.
- JS will use one core machine at a time.
- Cons: Bad language for scalable system.
- There is way to achieve to make it use all cores using **clustered module** [Learn more](https://www.geeksforgeeks.org/how-does-the-cluster-module-work/)


# Write Some Code

**Note** The following basic programs are skipped in this readme.

```
    1. write a program to print name and age of a person
    2. write a program to print number from 1 to 100
    3. write a simple program using var, let and const
```

### write a function that takes in two number and return the sum

```
    function sum(a, b) {
        const sumValues = a + b;
        return sum;
    }
    const value = sum(1,2);
    console.log(value) //3

```
### Bounty : How much cpu power will it take and why when the following js is execute (try in you local).

```
    let sum = 0;
    for(let i=0; i<100000000000000000; i++) {
        sum += i;
    }
    console.log(sum);

```

### write a function that takes another function as an argument

```
     function sum(a, b) {
        const sumValues = a + b;
        return sum;
    }

     function displayResults(data) {
        console.log("The result is:", data);
    }

     function displayResultPassive(data) {
        console.log("Sum's result is: ", data);
    }

    Follow up question: you are allowed to use only one function and display the result.How will you displayResult of sum.

```