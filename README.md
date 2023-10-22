# Studentgrade
import java.util.Scanner;

public class StudentGradeCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int numSubjects = 5; // You can change this to the number of subjects you have.
        int totalMarks = 0;

        System.out.println("Student Grade Calculator");
        System.out.println("Enter the marks for each subject:");

        for (int i = 1; i <= numSubjects; i++) {
            System.out.print("Subject " + i + " marks: ");
            int subjectMarks = scanner.nextInt();
            totalMarks += subjectMarks;
        }

        // Calculate the average percentage.
        double averagePercentage = (double) totalMarks / (numSubjects * 100) * 100;

        // Determine the result.
        String result = (averagePercentage >= 40) ? "Pass" : "Fail";

        // Display the results.
        System.out.println("\nTotal Marks: " + totalMarks);
        System.out.println("Average Percentage: " + averagePercentage + "%");
        System.out.println("Result: " + result);

        scanner.close();
    }
}
