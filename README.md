Download Link: https://assignmentchef.com/product/solved-datastructures-project1-sets
<br>
In this assignment, you are given two ADT interfaces, and you will implement them according to their specifications.

Starting point

<u>Download and extract these materials.</u> Contained are:

<ul>

 <li>java , the provided driver program.</li>

 <li>java , the things that will be held by a MovieShelf</li>

 <li>java , an exception type</li>

 <li>java and MovieShelfInterface.java , interfaces which you will implement in…</li>

 <li>java and MovieShelf.java . These are the files you will modify.</li>

</ul>

Do not modify anything other than Set.java and MovieShelf.java . We will be testing these with unmodified versions of the other files.

Organization is good. Make yourself a folder for this project if you haven’t already.

Set                                                            See the grading rubric

further down to see the

You will implement the Set class. It implements SetInterface . <sup>breakdown of the points. </sup>Read the doc comments for each method in SetInterface

carefully. In addition to the interface methods, you will also need to make some constructors, as detailed below.

<ul>

 <li>It will store its data in an array.</li>

 <li>It will be dynamic capacity (like we talked about in Lecture 3).</li>

 <li>The Set(int) constructor will initialize the array to the given capacity.</li>

</ul>

◦ It will check for an illegal capacity, and throw IllegalArgumentException in that case.

<ul>

 <li>The Set() constructor will initialize the array to a reasonable default capacity.</li>

</ul>

◦ Reusing methods/constructors is a great habit! See section D.10 of Carrano (page 877 in the 4th edition) for details.

<ul>

 <li>The Set(E[]) constructor will initialize the set to contain the items in the array.</li>

</ul>

◦ You will not make this array into the set’s backing array. That violates encapsulation.

◦ The array may contain duplicates and null s. You should ignore these instead of throwing an exception.

<ul>

 <li>Although you are given SetFullException , your add method will never actually throw it.</li>

</ul>

◦ Since your implementation will dynamically resize its capacity, it can never be “full.”

<h1>MovieShelf</h1>

You will implement the MovieShelf class. It implements MovieShelfInterface . Again, read the doc comments in that file carefully.

MovieShelf is a client of your Set . That is, it will have an instance <sub>You are writing code that </sub>of Set and use it to hold its data. This means you are creating this uses your own code. We class via composition.              call this “eating our own dogfood”. It’s kind of a gross

Details of your MovieShelf implementation                                                  term, but hey.

<ul>

 <li>It will store its data in a Set&lt;MovieShelfItem&gt; .</li>

 <li>The MovieShelf() constructor will initialize that Set to be empty.</li>

 <li>The MovieShelf(Movie[]) constructor will initialize that Set with that array of Movie s.</li>

 <li>A note on printAll() : you can use Set.toArray() to get the movies to print, but it is an array of Object . You will have to cast each item to a Movie to access its movie-specific getters.</li>

</ul>

<h1>Testing</h1>

We will be testing your code on the command line. You are welcome to use an IDE, but before submitting, please test that your Java files can be compiled and run on the command line without it.

You are given a simple driver program, but you should write your own driver as well to test your code more thoroughly. The driver provided does not test all the possible corner cases, and does not test Set directly.

<u>Click here for an example of what the driver will output for a correct implementation.</u>

This is not acceptable in this class or in your following classes. Comment out the code that doesn’t compile and put comments at the top of your Java files for the grader. You may receive some partial credit for such code.

Code that crashes may also receive partial credit.