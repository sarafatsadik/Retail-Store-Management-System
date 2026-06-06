# Retail-Store-Management-System
A smart retail management system that manages products, inventory, sales, customers, and billing operations to improve efficiency and simplify store management.

import java.util.Scanner;

public class RetailStoreManagement {

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        String product1 = "Rice";
        String product2 = "Milk";
        String product3 = "Sugar";

        double price1 = 80;
        double price2 = 90;
        double price3 = 120;

        int stock1 = 50;
        int stock2 = 30;
        int stock3 = 40;

        int choice;

        while(true) {

            System.out.println("\n===== Retail Store =====");
            System.out.println("1. View Products");
            System.out.println("2. Buy Product");
            System.out.println("3. Exit");

            System.out.print("Enter choice: ");
            choice = input.nextInt();


            if(choice == 1) {

                System.out.println("\nProduct List:");
                System.out.println("1. " + product1 +
                        " Price: " + price1 +
                        " Stock: " + stock1);

                System.out.println("2. " + product2 +
                        " Price: " + price2 +
                        " Stock: " + stock2);

                System.out.println("3. " + product3 +
                        " Price: " + price3 +
                        " Stock: " + stock3);

            }


            else if(choice == 2) {

                System.out.print("Enter product number: ");
                int product = input.nextInt();

                System.out.print("Enter quantity: ");
                int quantity = input.nextInt();


                if(product == 1) {

                    if(quantity <= stock1) {

                        double total = quantity * price1;
                        stock1 = stock1 - quantity;

                        System.out.println(
                        "Total Bill: " + total);

                        System.out.println(
                        "Purchase Successful");

                    } else {
                        System.out.println("Out of Stock");
                    }

                }


                else if(product == 2) {

                    if(quantity <= stock2) {

                        double total = quantity * price2;
                        stock2 -= quantity;

                        System.out.println(
                        "Total Bill: " + total);

                    } else {
                        System.out.println("Out of Stock");
                    }

                }


                else if(product == 3) {

                    if(quantity <= stock3) {

                        double total = quantity * price3;
                        stock3 -= quantity;

                        System.out.println(
                        "Total Bill: " + total);

                    } else {
                        System.out.println("Out of Stock");
                    }

                }


                else {
                    System.out.println("Invalid Product");
                }

            }


            else if(choice == 3) {

                System.out.println("Thank you!");
                break;

            }


            else {
                System.out.println("Invalid Choice");
            }

        }


        input.close();
    }
}
