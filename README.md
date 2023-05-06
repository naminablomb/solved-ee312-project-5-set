Download Link: https://assignmentchef.com/product/solved-ee312-project-5-set
<br>
This project will give you experience writing a data structure in C/C++. More importantly, you will get to put some serious effort into using good algorithms in your programs and analyzing their time complexity. Part of your grade for this project will be based on how efficient your programs are. We will attempt to ascertain if your algorithms require time proportional to <em>N<sup>2</sup>, N log<sub>2 </sub>N, N, </em>or <em>log<sub>2</sub>N</em>.




<strong>Your Mission: </strong>Edit the file “Project5.cpp”. You should not need to change any other files. You must implement all of the functions defined for the Set ADT (see Set.h for a complete list). I’ve taken care of several of these functions to get you started. However, the work that remains is <strong>substantial</strong>.  Get started early.

<strong>General Design: </strong>I suggest (actually, I insist) that you keep the elements inside the Set sorted. For example, whatever is stored in elements[0] should be smaller than any other element in the set.  Whatever is in elements[1] should be the second smallest, etc.

<strong>How Sets Work: </strong>Recall that a set is an unordered collection of things. Your Set class will hold a collection of <strong>int</strong>s. The operations you must implement include inserting and removing elements from the set. Please note that the same element <strong>cannot </strong>appear twice in the same set.  If <em>insertSet </em>is called where the parameter is a number that’s already in the set, your function should do nothing. Similarly, <em>removeSet </em>should remove an element from the set. If someone attempts to remove an element that’s not in the set, then you should do nothing.

In addition to inserting and removing elements, you must provide a membership test. In other words, it must be possible to determine if some arbitrary number is a member in your Set. The <em>isMemberSet </em>function should provide this capability. Two sets can also be compared. If the sets have exactly the same elements then they are equal. Note that two sets that each contain zero elements are equal.  A set, <em>X </em>is a subset of another set <em>Y </em>if all of the elements in <em>X </em>are also elements of <em>Y</em>. So, a set containing zero elements is a subset of every other set.  Also, every set is a subset of itself.

The interesting functions for sets are intersection, union and subtraction. Recall that the intersection of two sets is the elements that are common to both sets. So, if <em>X </em>has the elements {1, 3, 5, 7} and <em>Y </em>has the elements {1, 2, 3, 4} then the intersection of <em>X </em>and <em>Y </em>is a set with elements {1, 3}. The union of two sets is the set of elements that are in either one of the two sets. So, for the same <em>X </em>and <em>Y </em>above, the union would be a set containing {1, 2, 3, 4, 5, 7}.  Finally, set subtraction is defined as the set of all elements that are in the first set but are not in the second set. So, if we ask for <em>X – Y </em>we would compute the set containing {5, 7}.  You must write all three of these functions.




<strong>Performance: </strong>For this project we are interested in how efficiently your programs will run. Specifically we’re interested in determining for each function you write whether the function takes time proportional to the number of elements in the set, the logarithm of the number of elements in the set, or the square of the number of elements in the set. The best way to determine the efficiency of your algorithm is to analyze the code by hand and count how many operations must be performed. We’ll be trying to write a program that will automatically guess the performance. Such programs are very difficult to write, so don’t put too much faith in the estimates it gives (it almost always is wrong for isEqualTo). Do your own analysis (besides it will be a great way to study for the next test). For each of the following functions, the worst-case time complexity must be as described below:




<table width="0">

 <tbody>

  <tr>

   <td width="114">Function</td>

   <td width="421">Time Complexity (worst case, N is the number of elements in a set, for operations that apply to two sets, assume both sets have N elements).</td>

  </tr>

  <tr>

   <td width="114">insert</td>

   <td width="421">O(N)</td>

  </tr>

  <tr>

   <td width="114">remove</td>

   <td width="421">O(N)</td>

  </tr>

  <tr>

   <td width="114">isMember</td>

   <td width="421">O(log N)</td>

  </tr>

  <tr>

   <td width="114">isEqualTo</td>

   <td width="421">O(N) (not graded)</td>

  </tr>

  <tr>

   <td width="114">isSubsetOf</td>

   <td width="421">O(N)</td>

  </tr>

  <tr>

   <td width="114">unionIn</td>

   <td width="421">O(N)</td>

  </tr>

  <tr>

   <td width="114">intersectFrom</td>

   <td width="421">O(N)</td>

  </tr>

  <tr>

   <td width="114">subtractFrom</td>

   <td width="421">O(N)</td>

  </tr>

 </tbody>

</table>




<strong>Memory Leaks </strong>

Use Valgrind to check for memory leaks.  If your solution is implemented correctly, you should pass every test case, meet the above time complexity numbers, and have no memory leaks of any kind, when run on the ECE Linux server.




<strong>FAQ:   </strong>

Q: Do I need to check for well-formed input?

A: No, we will only pass in inputs that are well-formed.




Q: Will I be asked to merge two sets where they both point to the same place? A: No, see above.




<ol>

 <li>Do we have to check if realloc, calloc, or malloc returns a null ptr?</li>

</ol>

A: No, not for this or any other project, unless it is explicitly asked for, or unless the project is geared towards filling up the heap or some such stress test.




<ol>

 <li>Why aren’t the time complexities of insertSet and removeSet tested?</li>

 <li>We just did not do those. You should be able to look at your code to determine the time complexity.</li>

</ol>




<ol>

 <li>Running Valgrind causes my code to go from linear to super linear. Is this ok?</li>

 <li>Valgrind is probably slowing everything down. Your time complexities should be checked while not running Valgrind.</li>

</ol>




Q: I am seeing a memory leak even though I am sure I fixed everything.

“still reachable: 72,704 bytes in 1 blocks”

A: If you use Valgrind on the UT Linux machine you should not see this.  But, if you use Valgrind on some type of Linux Distro then you might have seen this.

<em> </em>

<em><u><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">http://stackoverflow.com/questions/30393229/new</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">–</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">libstdc</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">–</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">of</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">–</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">gcc5</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">–</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">1</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">–</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">may</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">–</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">allocate</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">–</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">large</a></u></em><em><u><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">heap</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">–</a><a href="https://stackoverflow.com/questions/30393229/new-libstdc-of-gcc5-1-may-allocate-large-heap-memory">memory</a></u></em><em>  </em>

<em> </em>

The reason “still reachable: 72,704 bytes in 1 blocks” doesn’t show up in the Linux servers is because they use an older version of GCC.




Q: Can we assume that all sets given to us will be ordered?




A: Yes. Our implementation of a set in C is an ordered list, and you will not have to check to make sure that this is the case.

Note, however, that even though the underlying structure is ordered, the user does not need to know about that. The ordering is just to make it faster to work with. When coding, remember that you are creating the mathematical concept of a set that has no order. So functions like subset should not pay attention to the order of the elements.




Q: Can we use standard C libraries?




A: Yes, you can if they are helpful, but they are not required. Remember that C++ libraries are not allowed. C libraries have a .h at the end and are included with &lt; &gt;.

Q: So throughout Project5.cpp there are many functions that return the bool type rather than an integer to represent true/false. Does this mean that for this project we can use booleans?

A: Yes, just use boolean type.

Notes: This lab is much more concerned with time complexity than space complexity, so wasting a little space is fine.




It might be helpful to make maximum_set_size smaller in main for testing purposes. When you’re done testing and fixing bugs, though, make sure to change it back to 100 and retest.


