# Assignment week 11 - Exploring the filesystem

Each section builds on the last. You should use the template at the bottom of this file to do your homework with (however you may choose to solve this any way to fully completes the assignment).

[Intro youtube video for the homework](https://youtu.be/OZKU_gqjrQI)


## Part 1 - Does the file exist?

  1. Create a new class called HomeworkWeek11 with a "public static void main(String args [])" method because you will run it directly.
  2. Prompt the user to type a filename or filepath. We are going to save the user input and check if this file exists.
  3. Check if what the user typed is a valid path. If not, have the user re-enter it.
  4. When the user types a valid path, use Files.exists() to see if the path exists.
  5. If the path exists, print something to the console that says so. If not, let the user know that also and force the user to enter a path that exists.


## Part 2 - What kind of file is it?

  1. You should now have a valid, existing file path from Part 1. You are now going to read the file attributes for the path. Create a "BasicFileAttributes" object using Files.readAttributes().
  2. Using the BasicFileAttributes object please print out the following information about the file:
    1. Name of file
    2. full path of file
    3. size of the file
    4. Is the file a directory? If not is it a normal file? 
    5. When was the file created?
    6. When was the file modified?
  3. If the file was NOT A DIRECTORY MAKE THE USER ENTER ANOTHER PATH! This means you must repeat Part 1 if the file is not a directory.  


## Part 3 - List the contents of a directory, and tell us about what is inside of it (NOT RECURSIVELY!!!)

  1. You should now have a file path that is: valid, does exist, and is a directory. If that is not the case you need to prompt the user to enter filepath that is a directory. 
  2. Once the user enters a valid, existing directory, list the contents of the directory and display this to the user. Make sure to print out the filename of each file in the directory.
  3. Count how many plain files (isRegularFile() on BasicFileAttributes) there are inside of the directory, print the count. YOU DO NOT NEED TO DO THIS RECURSIVELY! 
  4. Count how many directories are inside of this dir, print the count. YOU DO NOT NEED TO DO THIS RECURSIVELY!
  5. what is the most recently created file in this dir? Print it out. YOU DO NOT NEED TO DO THIS RECURSIVELY!
  6. What is the oldest file in this dir? Print it out. YOU DO NOT NEED TO DO THIS RECURSIVELY!
  
  
 ### Starting template for This homework
 
 ```java
 import java.nio.file.Path;
import java.util.Scanner;

public class ExploringTheFileSystemHomeworkStart {

	Scanner scanner = new Scanner(System.in);
	
	public static void main(String[] args) {
		
		boolean isADir = false;
		Path path = null;
		while(!isADir) {
			path = part1();
			isADir = part2(path);
			// do some logic to repeat part 1 if we did not get a dir.
		}
		
		part3(path);
	}
	
	public static Path part1() {
		
		// put logic for part1
		
		return null;
	}
	
	public static boolean part2(Path path) {
		
		// part 2 logic
		
		return false;
	}
	
	
	// should have a valid, existing, directory file path!
	public static void part3(Path path) {
		
		// part 3 logic
		
	}
	
	

}
```
