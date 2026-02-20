# object-oriented-prog-2-second-code
students code
import java.util.Scanner;

// i) Create a class named StudentRecord
class StudentRecord {
    // Three fields to store student details
    String studentID;
    String name;
    String course;

    // Constructor to initialize these fields
    public StudentRecord(String studentID, String name, String course) {
        this.studentID = studentID;
        this.name = name;
        this.course = course;
    }

    // Method to print the student details
    public void displayInfo() {
        System.out.println("\n--- Student Details ---");
        System.out.println("Student ID: " + studentID);
        System.out.println("Name: " + name);
        System.out.println("Course: " + course);
    }
}

// ii) Create another class named StudentApp
public class StudentApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to input their details
        System.out.print("Enter Student ID: ");
        String id = scanner.nextLine();

        System.out.print("Enter Name: ");
        String name = scanner.nextLine();

        System.out.print("Enter Course: ");
        String course = scanner.nextLine();

        // Instantiate a StudentRecord object using user-provided data
        StudentRecord student = new StudentRecord(id, name, course);

        // Call the displayInfo method
        student.displayInfo();
        
        scanner.close();
    }
}
