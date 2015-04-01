import TerminalIO.KeyboardReader;

public class Node {
	char letter;
	Node nodeptr;
	
	Node(){
		letter = ' ';
		nodeptr = null;
	}
	
	Node(char x, Node y){
		letter = x;
		nodeptr = y;
	}
	
	public static void AddLinear(Node start){
		KeyboardReader reader = new KeyboardReader();
		Node chain = new Node();
		char answer = 'n';
		
		start.nodeptr = new Node();
		chain = start.nodeptr;
		do{
			chain.letter = reader.readChar("\nEnter a letter: ");
			Print(start);
			answer = reader.readChar("Would you like to enter another letter(Y/N) ");
			if ((answer == 'Y')||(answer == 'y')){
				chain.nodeptr = new Node();
				chain = chain.nodeptr;
			}
		}while ((answer == 'Y')||(answer == 'y'));
		Print(start);
	}
	
	public static void Bubble(Node start){
		Node temp = new Node();
		boolean check = false;
		char tem;
		temp = start;
		while (check == false){
			temp = start;
			check = true;
			while (temp.nodeptr != null){
				if (Character.getNumericValue(temp.letter) > Character.getNumericValue(temp.nodeptr.letter)){
					tem = temp.letter;
					temp.letter = temp.nodeptr.letter;
					temp.nodeptr.letter = tem;
					check = false;
				}
				temp = temp.nodeptr;
			}
		}
		System.out.print("Sorted ");
		Print(start);
	}
	
	public static void SortList(Node start){
		KeyboardReader reader = new KeyboardReader();
		char answer = 'n', letter = 'a';

		letter = reader.readChar("\nEnter a letter: ");
		start.letter = letter;
		Node.Print(start);
		answer = reader.readChar("Would you like to enter another letter(Y/N) ");

		if ((answer == 'Y')||(answer == 'y')){
			Node cntr = new Node();
			boolean checker = false;

			do{
				Node temp = new Node();
				temp.letter = reader.readChar("\nEnter a letter: ");
				cntr = start;
				checker = false;

				while (checker == false){
					if (start.letter >= temp.letter){
						temp.nodeptr = start;
						start = temp;
						checker = true;
					}
					else if (cntr.nodeptr == null){
						cntr.nodeptr= new Node();
						cntr.nodeptr.letter = temp.letter;
						checker = true;
					}
					else if ((cntr.letter <= temp.letter)&&(cntr.nodeptr.letter >= temp.letter)){
						temp.nodeptr = cntr.nodeptr;
						cntr.nodeptr = temp;
						checker = true;
					}
					else if (checker == false)
						cntr = cntr.nodeptr;
				}
				Node.Print(start);
				answer = reader.readChar("Would you like to enter another letter(Y/N) ");
			}while ((answer == 'Y')||(answer == 'y'));
		}
		Node.Print(start);
	}
	
	public static void Print(Node start){
		Node temp = new Node();
		System.out.print("Linked list: ");
		temp = start;
		while (temp != null){
			System.out.print(temp.letter);
			temp = temp.nodeptr;
		}
		System.out.println();
	}
}
