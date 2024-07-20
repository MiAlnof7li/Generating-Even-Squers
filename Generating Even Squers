import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;
import java.util.stream.Collectors;

public class ListOperations {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input the list of integers
        System.out.print("Enter the list of integers (space-separated): ");
        String input = scanner.nextLine();
        String[] inputArray = input.split(" ");
        List<Integer> originalList = new ArrayList<>();

        for (String numStr : inputArray) {
            try {
                originalList.add(Integer.parseInt(numStr));
            } catch (NumberFormatException e) {
                System.out.println("Invalid input: " + numStr);
                return;
            }
        }

        // Create a list of squares of even numbers using Streams
        List<Integer> evenSquaresList = originalList.stream()
                .filter(num -> num % 2 == 0) // Filter even numbers
                .map(num -> num * num) // Square the numbers
                .collect(Collectors.toList()); // Collect the results into a list

        System.out.println("List of squares of even numbers: " + evenSquaresList);

        // Input the start and end indices for slicing
        System.out.print("Enter the start index: ");
        int startIndex = scanner.nextInt();

        System.out.print("Enter the end index: ");
        int endIndex = scanner.nextInt();

        if (startIndex < 0 || endIndex > originalList.size() || startIndex > endIndex) {
            System.out.println("Invalid indices. Please enter valid start and end indices.");
        } else {
            List<Integer> subList = originalList.subList(startIndex, endIndex);
            System.out.println("Sliced list: " + subList);
        }
    }
}
