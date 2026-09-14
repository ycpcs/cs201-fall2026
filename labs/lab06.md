---
layout: default
title: "Lab 6: Text File I/O"
---

## Getting Started

Download [CS201\_Lab06\_Gradle.zip](CS201_Lab06_Gradle.zip). Copy and extract the zip file into your **CS201-Fall2026** directory. Import it into your **CS201-Fall2026** IntelliJ project using

> **open**

Select the **CS201\_Lab06\_Gradle** directory and click **select folder**.

You should see a project called **CS201\_Lab06\_Gradle** in the Project window.

Run the program by right-clicking on the file **Remember.java** in the **src/main/java/** directory, and then choosing

> **Run 'Remember.main()'**

Or subsequently by selecting **Remember** from the dropdown list in the top right corner of the IDE and clicking the green arrow.

Here is an example session showing what should happen the *first* time someone runs the program (user input in **bold**):

<pre>
No one has run this program before!
What is your name? <b>Alice</b>
Ok, Alice, I'm writing your name to a file
</pre>

An example session showing what happens the *second* time someone runs the program (user input in **bold**):

<pre>
The last person to run the program was Alice
What is your name? <b>Bob</b>
Ok, Bob, I'm writing your name to a file
</pre>

The next time someone runs the program, it will print Bob's name as the last person to run the program.

## Hints

Store the name of the last person to run the program in a text file.

You can use a **FileReader** and **BufferedReader** to read from the file, and a **FileWriter** to create the file.

You will need to be able to determine whether or not the file containing the name has been created. You can do so as follows. The variable **fileName** is a String which is provided that contains the filename (and path) in which the name should be stored:

    File f = new File(fileName);
    if (f.exists()) {
        // the file exists
    } else {
        // the file has not been created yet
    }

Once the file is created, it should appear in the **CS201\_Lab06\_Gradle** directory.

## Submitting

When you are done, submit the lab to the Marmoset server using the **plugin** in IntelliJ.
