---
layout: default
title: "Lab 12: Functors"
---

## Getting Started

Download [CS201\_Lab12\_Gradle.zip](CS201_Lab12_Gradle.zip). Copy and extract the zip file into your **CS201-Fall2026** directory. Import it into your **CS201-Fall2026** IntelliJ project using

> **Open**

Select the **CS201\_Lab12\_Gradle** directory and click **Select Folder**.

You should see a project called **CS201\_Lab12\_Gradle** in the Project window.

**There is no executable application for this lab.** Instead, we will test the class implementation by running the unit tests by right-clicking on the file **CountJFunctorTest.java** and **SumIntFunctorTest** in the **src/test/java/** directory, and then choosing

> **Run 'CountJFunctorTest'**

(and similarly for **SumIntFunctorTest**). Or subsequently by selecting **CountJFunctorTest**, etc. from the dropdown list in the top right corner of the IDE and clicking the green arrow.

## A Generic Functor interface

The **Functor** interface defines a very simple kind of functor: one that takes a single argument value, performs some computation on it, and stores the result of the computation in a field or fields:

{% highlight java %}
public interface Functor<E> {
    /**
     * Apply the functor to a value.
     * 
     * @param value a value
     */
    public void apply(E value);
}
{% endhighlight %}

The **ApplyFunctor** class contains a single generic method which is useful for working with **Functor** instances:

{% highlight java %}
public static<E> void applyToArray(E[] arr, Functor<E> functor) {
    for (int i = 0; i < arr.length; i++) {
        functor.apply(arr[i]);
    }
}
{% endhighlight %}

The **applyToArray** method takes an array of elements of type **E** and a **Functor&lt;E&gt;**, and calls the functor's **apply** method on each element of the array. This function may be used to perform a computation on all of the elements in an array.

## Your Task

Your task is to implement two classes which implement the **Functor** interface:

1.  **SumIntFunctor**, which implements **Functor&lt;Integer&gt;**. It computes the sum of all of the **Integer** values to which it is applied.
2.  **CountJFunctor**, which implements **Functor&lt;String&gt;**. It computers the number of occurrences of the characters 'J' and 'j' in the **String** values to which it is applied.

The **SumIntFunctorTest** and **CountJFunctorTest** classes implement JUnit tests for both classes.

## Hints

The **SumIntFunctor** and **CountJFunctor** classes should build up the overall result by updating the value of a field or fields.

## Submitting

When you are done, submit the lab to the Marmoset server using IntelliJ.
