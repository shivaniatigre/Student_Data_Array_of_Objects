# Student_Data_Array_of_Objects
 A menu-driven Java Program that studies the concepts of classes, array of objects, instance members, constructors in java. 
import java.util.ArrayList;
import java.util.Scanner;

// Student class with instance variables, constructor and methods
class Student {
private int prn;
private String name;
private String dob;
private float marks;

// Constructor to initialize instance variables
public Student(int prn, String name, String dob, float marks) {
    this.prn = prn;
    this.name = name;
    this.dob = dob;
    this.marks = marks;
}

// Getters and setters for instance variables
public int getPrn() {
    return prn;
}

public void setPrn(int prn) {
    this.prn = prn;
}

public String getName() {
    return name;
}

public void setName(String name) {
    this.name = name;
}

public String getDob() {
    return dob;
}

public void setDob(String dob) {
    this.dob = dob;
}

public float getMarks() {
    return marks;
}

public void setMarks(float marks) {
    this.marks = marks;
}

// Method to display student details
public void displayStudent() {
    System.out.println("PRN: " + prn + "\tName: " + name + "\tDoB: " + dob + "\tMarks: " + marks);
}
}

public class Main {
// Array list to store students
static ArrayList<Student> students = new ArrayList<>();
// Scanner object for user input
static Scanner scanner = new Scanner(System.in);

public static void main(String[] args) {
    int choice;
    do {
        // Display menu to user
        System.out.println("\nMENU:");
        System.out.println("1. Add student");
        System.out.println("2. Display all students");
        System.out.println("3. Search by PRN");
        System.out.println("4. Search by name");
        System.out.println("5. Search by position");
        System.out.println("6. Update student details");
        System.out.println("7. Delete student");
        System.out.println("8. Exit");
        System.out.print("Enter your choice: ");
        choice = scanner.nextInt();

        // Perform action based on user choice
        switch (choice) {
            case 1:
                addStudent();
                break;
            case 2:
                displayAllStudents();
                break;
            case 3:
                searchByPRN();
                break;
            case 4:
                searchByName();
                break;
            case 5:
                searchByPosition();
                break;
            case 6:
                updateStudentDetails();
                break;
            case 7:
                deleteStudent();
                break;
            case 8:
                System.out.println("Exiting...");
                break;
            default:
                System.out.println("Invalid choice! Please try again.");
                break;
        }
    } while (choice != 8);
}

// Method to add a new student
public static void addStudent() {
    System.out.print("\nEnter PRN: ");
    int prn = scanner.nextInt();
    System.out.print("Enter name: ");
    String name = scanner.next();
    System.out.print("
