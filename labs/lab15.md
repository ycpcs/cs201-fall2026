---
layout: default
title: "Lab 15: Iterators, Interleaving"
---

## Getting Started

Download [CS201\_Lab15\_Gradle.zip](CS201_Lab15_Gradle.zip). Copy and extract the zip file into your **CS201-Fall2026** directory. Import it into your **CS201-Fall2026** IntelliJ project using

> **Open**

Select the **CS201\_Lab15\_Gradle** directory and click **Select Folder**.

You should see a project called **CS201\_Lab15\_Gradle** in the Project window.

**There is no executable application for this lab.** Instead, we will test the class implementation by running the unit tests by right-clicking on the file **AlgorithmTest.java** in the **src/test/java/** directory, and then choosing

> **Run 'AlgorithmTest'**

Or subsequently by selecting **AlgorithmTest** from the dropdown list in the top right corner of the IDE and clicking the green arrow.

## Your Task

Your task is to implement two generic methods in the **Algorithm** class: **interleave** and **mergeSortedLists**. Each method takes references to two collections as parameters.

-   The **interleave** method takes two collections, uses iterators to traverse their elements, and returns a list in which the elements in the original collections are "interleaved". For example, if the collections are lists containing **(A, B, C)** and **(D, E, F)** respectively, the result will be a list containing **(A, D, B, E, C, F)**.
-   The **mergeSortedLists** method takes two sorted lists and returns a single list containing all of the elements in the two original lists, in sorted order. For example, if the original lists are **(1, 4, 5)** and **(2, 3, 6)** then the result list would be **(1, 2, 3, 4, 5, 6)**.

Each method is accompanied by a detailed documentation comment describing how the method should work, and providing hints.

The **AlgorithmTest** JUnit test class has unit tests for each method. Take a look at the tests if you are not sure about how the method is intended to work.

## Submitting

When you are done, submit the lab to the Marmoset server using IntelliJ.
