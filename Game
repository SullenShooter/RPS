package Random;
import java.util.Scanner;
import java.util.Random;

public class RPS {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        String[] options = {"rock", "paper", "scissors"};

        int playerScore = 0;
        int computerScore = 0;

        System.out.println("Welcome to Rock, Paper, Scissors!");
        System.out.println("Type 'quit' to exit.");

        while (true) {
            System.out.print("\nEnter your move (rock, paper, or scissors): ");
            String playerMove = scanner.nextLine().trim().toLowerCase();

            if (playerMove.equals("quit")) {
                System.out.println("\nFinal Score: You " + playerScore + " – Computer " + computerScore);
                System.out.println("Thanks for playing!");
                break;
            }

            // Validate user input
            if (!playerMove.equals("rock") && !playerMove.equals("paper") && !playerMove.equals("scissors")) {
                System.out.println("Invalid input. Please enter rock, paper, scissors, or quit.");
                continue;
            }

            // Computer's move
            String computerMove = options[random.nextInt(3)];
            System.out.println("Computer chose: " + computerMove);

            // Determine the winner
            if (playerMove.equals(computerMove)) {
                System.out.println("It's a tie!");
            } else if (
                (playerMove.equals("rock") && computerMove.equals("scissors")) ||
                (playerMove.equals("paper") && computerMove.equals("rock")) ||
                (playerMove.equals("scissors") && computerMove.equals("paper"))
            ) {
                System.out.println("You win this round!");
                playerScore++;
            } else {
                System.out.println("Computer wins this round.");
                computerScore++;
            }

            // Display current score
            System.out.println("Current Score: You " + playerScore + " – Computer " + computerScore);
        }

        scanner.close();
    }
}
