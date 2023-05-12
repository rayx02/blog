---
title: Языки научного программирования
subtitle: Языки научного программирования C

# Summary for listings and search engines
summary: Здесь вы можете узнать немного больше о языке программирования C

# Link this post with a project
projects: []

# Date published
date: '2023-05-12T00:00:00Z'

# Date updated
lastmod: '2023-05-12T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**prince**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin
  - 吳恩達

tags:
  - Academic
  - 开源

categories:
  - Demo
  - 教程
---

## Introduction to the C language

- The C programming language was created by Dennis Ritchie of AT&T Bell Laboratories as a high-level programming language for developing the UNIX operating system. Currently, the language is widely used in various fields. C is especially popular with system programmers because it allows you to write programs simply and concisely.

The main book describing the C language is the book by Brian Kernighan and Dennis Ritchie “The C Programming Language” (1978). Books on the C language were written by Bolon (1986), Gehani (1984), Hancock and Krieger (1986), Harbison and Steele (1984) and many others.

In this appendix, we will try to give a fairly complete introduction to C, so that those who are familiar with high-level languages such as Pascal, PL/1 or Modula 2 will be able to understand most of the MINIX code given in this book. C features that are not used in MINIX are not discussed here. Numerous subtle points are omitted. The emphasis is on reading C programs, not writing code.

## Basics of the C language

- A C program consists of a set of procedures (often called functions, even if they do not return values). These procedures contain declarations, operators, and other elements that together tell the computer what to do. Figure A-1 shows a small procedure in which three integer variables are declared and values are assigned to them. The name of the procedure is main. The procedure has no formal parameters, as indicated by the absence of any identifiers between the brackets behind the procedure name. The procedure body is enclosed in curly brackets ( { } ). This example shows that C has variables, and that these variables must be declared before use. C also has operators, in this example these are assignment operators. All operators must end with a semicolon (unlike Pascal, who uses colons between operators, not after them). Comments start with the characters " / " and end with the characters “ /” and can take up several lines.

## Итоги
- Basic Data types

Programs operate with various data, which can be simple and structured. Simple data is integers and real numbers, symbols and pointers (addresses of objects in memory). Integers do not have, and real numbers have a fractional part. Structured data is arrays and structures; they will be discussed below.

The language distinguishes between the concepts of “data type” and “type modifier”. A data type is, for example, an integer, and a modifier is signed or unsigned. A signed integer will have both positive and negative values, and an unsigned integer will have only positive values. In the C language, five basic types can be distinguished, which are defined by the following keywords: char - character; int - whole; float - real; double - real double precision; void - doesn’t matter.

Let’s give them a brief description:

A variable of type char has a size of 1 byte, its values are various characters from the code table, for example: ‘f’, ‘:’, ‘j’ (when written in the program, they are enclosed in single quotes). The size of an int type variable is not defined in the C language standard. In most programming systems, the size of an int variable corresponds to the size of an entire machine word. For example, in compilers for 16-bit processors, an int variable has a size of 2 bytes. In this case, the signed values of this variable can range from -32768 to 32767. The float keyword allows you to define variables of real type. Their values have a fractional part separated by a dot, for example: -5.6, 31.28, etc. Real numbers can also be written in floating point form, for example: -1.09e+4. The number before the symbol “e” is called the mantissa, and after the “e” - the order. A variable of the float type occupies 32 bits in memory. It can take values in the range from 3.4e-38 to 3.4e+38. The double keyword allows you to define a double-precision real variable. It takes up twice as much space in memory as a float variable (i.e. its size is 64 bits). A double variable can take values in the range from 1.7e-308 to 1.7e+308. The void keyword (meaningless) is used to neutralize the value of an object, for example, to declare a function that does not return any values. An object of some basic type can be modified. For this purpose, special keywords called modifiers are used. The C ANSI standard has the following type modifiers:

    unsigned

    signed

    short

    long

Modifiers are written before type specifiers, for example: unsigned char. If a specifier is omitted after the modifier, then the compiler assumes that this specifier is int. Thus, the following lines:

    long a;

    long int a;

are identical and define object a as a long integer. Table 1 illustrates possible combinations of modifiers (unsigned, signed, short, long) with specifiers (char, int, float and double), and also shows the size and range of object values (for 16-bit compilers).

Released under the [MIT](https://github.com/wowchemy/wowchemy-hugo-themes/blob/master/LICENSE.md) license.

