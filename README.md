Download Link: https://assignmentchef.com/product/solved-cse-522-assignment-5-part-2-design-by-contract
<br>
Posted on Piazza:Resources à Assignments is a zip file CFJ_BST_Iter.zip.  Unzip this file to obtain a directory CFJ_BST_Iter containing a fully configured project which you may import into Eclipse by doing: File à Import à Existing Projects into Workspace.   The added configurations permit the inclusion of CoFoJa contract annotations in the Java source.

The imported project contains a file BST_Contract.java with the familiar Tree and DupTree classes along with a class BST_Iterator which works on both trees and duptrees.  The class DupTree extends Tree and the values in both types of trees are integers.   Also included is an @Invariant(ordered()) clause for class Tree.

Your task in this part of the assignment is to write CoFoJa contracts (@Requires and @Ensures annotations) for the constructor of BST_Iterator and the two methods that modify its state, namely, next() and stack_left_spine().

<strong><em>Writing Contracts.</em></strong>  The contracts should capture the basic requirements and properties of the iterator, namely, that:

<ol>

 <li>the iterator only works on binary search trees;</li>

 <li>the values are returned in ascending order; and</li>

 <li>the stack invariant (described in Lecture 9) is maintained.</li>

</ol>

Your contracts may refer to the fields count, value and stack of BST_Iterator as well as <em>functions that do not modify the state</em> of any object, such as Tree.min(), Tree.max(),

Tree.ordered(), Stack.isEmpty(), Stack.peek(), BST_Iterator.hasNext(), etc.




<strong><em>Running the Program.</em></strong>  In order to run your program, you need to give the name of the .jar file in the VM Arguments of the Run Configuration, as follows:




-javaagent:lib/cofoja+asm-1.3.1-20170424.jar




Run BST_Contract.java augmented with contracts and ensure that the program works correctly.


