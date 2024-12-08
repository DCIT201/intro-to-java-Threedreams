public class TemperatureConverter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Welcome to the Temperature Converter!");
        System.out.println("Choose an option:");
        System.out.println("1. Convert Celsius to Fahrenheit");
        System.out.println("2. Convert Fahrenheit to Celsius");

        int choice = scanner.nextInt();

        // Ensure the user enters a valid choice
        if (choice != 1 && choice != 2) {
            System.out.println("Invalid option. Please restart the program and choose either 1 or 2.");
            return;
        }

        System.out.print("Enter the temperature value: ");
        double inputTemp = scanner.nextDouble();
        double convertedTemp;

        if (choice == 1) {
            // Celsius to Fahrenheit
            convertedTemp = (inputTemp * 9 / 5) + 32;
            System.out.printf("%.2f°C is equal to %.2f°F\n", inputTemp, convertedTemp);
        } else {
            // Fahrenheit to Celsius
            convertedTemp = (inputTemp - 32) * 5 / 9;
            System.out.printf("%.2f°F is equal to %.2f°C\n", inputTemp, convertedTemp);
        }

        System.out.println("Thank you for using the Temperature Converter!");
    }
}
