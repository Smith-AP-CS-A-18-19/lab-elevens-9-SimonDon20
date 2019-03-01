# Elevens 9

Follow the instructions provided for Activity 9 in the student lab guide. Complete the necessary methods and ensure that your game is running properly. You may need to run it from the command line to have it recognize the card graphics. Answer the questions below before you push the finalized repo.

## Questions
1. The size of the board is one of the differences between *Elevens* and *Thirteens*. Why is size not an abstract method?

    * Because the two games vary in board size, they cannot be abstract method since these methods are not implemented.

2. Why are there no abstract methods dealing with the selection of the cards to be removed or replaced in the array `cards`?

    * The selection and removal methods do not have to be abstract since those methods are common for each game.

3. Another way to create “IS-A” relationships is by implementing interfaces. Suppose that instead of creating an `abstract Board` class, we created the following `Board` interface, and had `ElevensBoard` implement it. Would this new scheme allow the Elevens GUI to call `isLegal` and `anotherPlayIsPossible` polymorphically? Would this alternate design work as well as the `abstract Board` class design? Why or why not?
	```java
	public interface Board {
	    boolean isLegal(List<Integer> selectedCards);
	    boolean anotherPlayIsPossible();
	}
	```

    * Yes it would because the methods expressed in the interface are already written. It works similarly to the abstract board, for the abstract has no implementation, and the interface is empty. ElevensBoard can access the methods in the interface because it implements Board.
