How to display an ArrayList in GUI

Create ArrayListGUI class that extends JFrame 
  Add Member Variables
    ArrayList<Integer> list //to store the arrayList
    Jbuttons called ‘add’, ‘remove’, ‘find’, ‘sort’
    JTextField called text1
    JTable called table 
    JScrollPane called scroll //used to add a scroll to the table
  Constructor
    Create the JFrame by setting its size, close operations, setting its layout to GridBagLayout, and initializing a    
      GridBagConstraints to help with placements
    Add to the frame a JLabel called title that writes “ArrayList!!” in the       gridx = 0 gridy = 0
    Add text1 to the frame at gridx = 0 gridy = 1
    Add the add JButton to the frame at gridx = 1 gridy = 1 and in the actionlistener make it call the addToList method and 
      read text1 for the int input
    Add the find JButton to the frame at gridx = 2 gridy = 1 and in the actionlistener make it call the finding method and 
      read text1 for the int input
    Add the remove JButton to the frame at gridx = 3 gridy = 1 and in the actionlistener make it call the remove method and 
      read text1 for the int input
    Add the sort Jbutton to the frame at gridx = 5 gridy = 1 and in the actionlistener make it call the sort method
    setVisible to true
  Void AddToList(int num, GridBagConstraints c)
    Add ‘num’ to ‘list’
    Call print method to print entire ‘list’ to table
  Void finding(int num, GridBagConstraints c)
    Create a temporary arraylist
    Find all instances of ‘num’ in ‘list’ and add each instance to the temp arraylist
    Call print method to print the instances to the table
  Void remove(int num, GridBagConstraints c)
    Iterate through ‘list’ in a for-loop removing each instance of num found
    Call print method to print entire ‘list’
  Void sort(GridBagConstraints c)
    Copy ‘list’ to an int array
    Sort int array using insertion sort (or another sorting method)
    Find the indexes of the sorted numbers and copy the indexes in order into a temporary arraylist
    Call print method to print entire sorted array
  Void print(ArrayList<Integer> x, GridBagConstraints c, boolean all)
    Try removing any table that is already there
    Create a String array for column headers of table
    Get the size of Arraylist ‘x’ and use it to initialize a 2D int array
    Populate the 2d array with the indexes and numbers from ‘x’ if ‘all’ is true
    If ‘all’ is false then populate the 2d array with the indexes from ‘x’ and the numbers from ‘list’ that correspond to 
      those indexes
    Add table to ‘scroll’ and then add ‘scroll’ to the frame and set visible
Create a Main Class to run the program
  Create a main method that just initializes the object of the ArrayListGUI class
