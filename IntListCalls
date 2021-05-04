// ****************************************************************
// IntListCalls.java                          Ken Haight
// Purpose: Defines a class that represents a list of integers 
// ****************************************************************
public class IntListCalls
{

    private IntNode front;      //first node in list

    //-----------------------------------------
    //  Constructor.  Initially list is empty.
    //-----------------------------------------
    public IntList()
    {
	front = null;
    }

    //-----------------------------------------
    //   Adds given integer to front of list.
    //-----------------------------------------
    public void addToFront(int val)
    {
	front = new IntNode(val,front);
    }


    //--------------------------------------
    //   Adds given integer to end of list.
    //--------------------------------------
    public void addToEnd(int val)
    {
	IntNode newnode = new IntNode(val,null);

	//if list is empty, this will be the only node in it
	if (front == null)
	    front = newnode;
	else
	    {
		//make temp point to last thing in list
		IntNode temp = front;
		while (temp.next != null)
		    temp = temp.next;

		//link new node into list
		temp.next = newnode;
	    }
    }


    //-------------------------------------------
    //   Removes the first node from the list.
    //   If the list is empty, does nothing.
    //-------------------------------------------
    public void removeFirst()
    {
	if (front != null)
	    front = front.next;
    }



    //------------------------------------------------
    //   Prints the list elements from first to last.
    //------------------------------------------------
    public void print()
    {

	System.out.println("---------------------");
	System.out.print("List elements: ");

	IntNode temp = front;

	while (temp != null)
	    {
		System.out.print(temp.val + " ");
		temp = temp.next;
	    }
	System.out.println("\n---------------------\n");

    }


    //----------------------------------------------------
    //  Prints the list recursively.
    //----------------------------------------------------
    public void printRec()
    {
	System.out.println ("\nList Elements...");
	printRec(front);
    }

    //----------------------------------------------------
    //  Recursively prints the part of the list starting 
    //  starting at the node pointed to by first.
    //---------------------------------------------------- 
    private void printRec (IntNode first)
    {
	if (first == null)
	    System.out.println();
	else
	    {
		System.out.print (first.val + " ");
		printRec(first.next);
	    }
    }


    //----------------------------------------------------
    //  Prints the list backwards using recursion.
    //----------------------------------------------------
    public void printRecBackwards()
    {
	System.out.println ("\nThe list backwards...");
	printRecBackwards(front);
    }

    //---------------------------------------------------
    //  Recursively prints the part of the list starting
    //  at the node pointed to by first backwards.
    //---------------------------------------------------
    private void printRecBackwards(IntNode first)
    {
	if (first != null)
	    {
		printRecBackwards(first.next);
		System.out.print(first.val + " ");
	    }
    }


    //***************************************************************
    // An inner class that represents a node in the integer list.
    // The public variables are accessed by the IntList class.
    //***************************************************************
    private class IntNode
    {
	public int val;         //value stored in node
	public IntNode next;    //link to next node in list

    //-------------------------------------------------------------------
    // Constructor; sets up the node given a value and IntNode reference
    //-------------------------------------------------------------------
	public IntNode(int val, IntNode next)
	{
	    this.val = val;
	    this.next = next;
	}
    }
}
