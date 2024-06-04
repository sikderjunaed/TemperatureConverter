import java.util.Scanner;

public class TemperatureConverter {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        boolean exit = false;

        while (!exit) {
            System.out.println("Temperature Converter");
            System.out.println("1. Celsius to Fahrenheit");
            System.out.println("2. Fahrenheit to Celsius");
            System.out.println("3. Celsius to Kelvin");
            System.out.println("4. Kelvin to Celsius");
            System.out.println("5. Fahrenheit to Kelvin");
            System.out.println("6. Kelvin to Fahrenheit");
            System.out.println("7. Exit");
            System.out.print("Choose an option: ");
            int choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    System.out.print("Enter temperature in Celsius: ");
                    double celsius = scanner.nextDouble();
                    System.out.println("Temperature in Fahrenheit: " + celsiusToFahrenheit(celsius));
                    break;
                case 2:
                    System.out.print("Enter temperature in Fahrenheit: ");
                    double fahrenheit = scanner.nextDouble();
                    System.out.println("Temperature in Celsius: " + fahrenheitToCelsius(fahrenheit));
                    break;
                case 3:
                    System.out.print("Enter temperature in Celsius: ");
                    celsius = scanner.nextDouble();
                    System.out.println("Temperature in Kelvin: " + celsiusToKelvin(celsius));
                    break;
                case 4:
                    System.out.print("Enter temperature in Kelvin: ");
                    double kelvin = scanner.nextDouble();
                    System.out.println("Temperature in Celsius: " + kelvinToCelsius(kelvin));
                    break;
                case 5:
                    System.out.print("Enter temperature in Fahrenheit: ");
                    fahrenheit = scanner.nextDouble();
                    System.out.println("Temperature in Kelvin: " + fahrenheitToKelvin(fahrenheit));
                    break;
                case 6:
                    System.out.print("Enter temperature in Kelvin: ");
                    kelvin = scanner.nextDouble();
                    System.out.println("Temperature in Fahrenheit: " + kelvinToFahrenheit(kelvin));
                    break;
                case 7:
                    exit = true;
                    System.out.println("Exiting...");
                    break;
                default:
                    System.out.println("Invalid choice. Please choose again.");
            }
            System.out.println();
        }
        scanner.close();
    }
    public static double celsiusToFahrenheit(double celsius) {
        return (celsius * 9 / 5) + 32;
    }
    public static double fahrenheitToCelsius(double fahrenheit) {
        return (fahrenheit - 32) * 5 / 9;
    }
    public static double celsiusToKelvin(double celsius) {
        return celsius + 273.15;
    }
    public static double kelvinToCelsius(double kelvin) {
        return kelvin - 273.15;
    }
    public static double fahrenheitToKelvin(double fahrenheit) {
        return (fahrenheit - 32) * 5 / 9 + 273.15;
    }

    public static double kelvinToFahrenheit(double kelvin) {
        return (kelvin - 273.15) * 9 / 5 + 32;
    }
}
