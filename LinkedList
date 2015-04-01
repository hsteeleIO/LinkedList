import TerminalIO.KeyboardReader;

public class LinkedList {

	public static void main(String[] args) {
		KeyboardReader reader = new KeyboardReader();
		Node start = new Node();
		int choice;
		
		System.out.println("What would you like to do? ");
		System.out.println("(1) Input a linked list ");
		System.out.println("(2) Build a linked list in alphabetical order");
		System.out.println("(3) Bubble sort a linked list");
		choice = reader.readInt("Input your choice: ");
		switch(choice){
			case 1:Node.AddLinear(start);break;
			case 2:Node.SortList(start);break;
			case 3:Node.AddLinear(start);Node.Bubble(start);break;
			default: System.out.println("This is not a valid choice");break;
		}

		System.out.println("\nThank you for using this program.");

	}

}
