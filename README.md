import java.util.Scanner;
public class OnlinExamination {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        // Mock questions and answers (for simplicity)
        String[] questions = {
            "1. What is the capital of France?\nA. Paris\nB. London\nC. Berlin\n",
            "2. Which planet is known as the Red Planet?\nA. Venus\nB. Mars\nC. Jupiter\n",
            "3. Who wrote 'Hamlet'?\nA. William Shakespeare\nB. Charles Dickens\nC. Jane Austen\n"
        };
        String[] correctAnswers = {"A", "B", "A"};
        int score = 0;
        System.out.println("Welcome to the Online Exam System!\n");
        // Ask each question
        for (int i = 0; i < questions.length; i++) {
            System.out.println(questions[i]);
            System.out.print("Your answer (Enter A, B, or C): ");
            String answer = scanner.nextLine().toUpperCase();
            // Validate answer and calculate score
            if (answer.equals(correctAnswers[i])) {
                System.out.println("Correct!\n");
                score++;
            } else {
                System.out.println("Incorrect. The correct answer is " + correctAnswers[i] + ".\n");
            }
        }
        // Display final score
        System.out.println("Exam completed! Your final score is: " + score + " out of " + questions.length);
        // Close the scanner
        scanner.close();
    }
}

