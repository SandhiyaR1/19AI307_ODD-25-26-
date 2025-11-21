# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:
To write a Java program using inheritance where a base class Customer stores customer details and calculates gold purchase price, while derived classes RegularCustomer and PremiumCustomer apply different discount rates. The program should calculate the final price based on gold rate per gram and show cashback for premium customers.

## ALGORITHM :
1.Start the program.

2.Define the Customer base class with:

Attributes: customerId, name, purchaseWeight, goldRatePerGram

Methods:

getDiscountRate() — returns 0 for general customers

calculateFinalPrice() — computes final price after discount

display() — displays details for a general customer

Create RegularCustomer class extending Customer:

Override getDiscountRate() to return 2%

Override display() to show Regular customer details

3.Create PremiumCustomer class extending Customer:

Override getDiscountRate() to return 5%

Add method calculateCashback() to compute 1% cashback

Override display() to show Premium customer details including cashback

4.In main():

Read customer type, id, name, purchase weight, and gold rate per gram.

If customer type is Regular, create a RegularCustomer object.

Else, create a PremiumCustomer object.

Call the display() method to show the final results.

5.End the program.


## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: SANDHIYA R
RegisterNumber:  212222230129
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer
{
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    int getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
     
    }
}
class RegularCustomer extends Customer
{
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram)
    {
        super(customerId,name,purchaseWeight,goldRatePerGram);
    }
    @Override
    int getDiscountRate() {
        return 2;
    }
    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}
class PremiumCustomer extends Customer
{
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram)
    {
        super(customerId,name,purchaseWeight,goldRatePerGram);
    }
    @Override
    int getDiscountRate() {
        return 5;
    }
    double calculateCashback(double final_price)
    {
        return final_price/100;
    }
    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        double final_price = calculateFinalPrice();
        System.out.println("Final Price: " + df.format(final_price));
        System.out.println("Cashback: " + df.format(calculateCashback(final_price)));

     
    }
    
}
public class Main
{
    public static void main(String[] args)
    {
        Scanner in=new Scanner(System.in);
        String customer_type=in.next();
        String id=in.next();
        String name=in.next();
        double purchaseweight=in.nextDouble();
        double goldRatePerGram=in.nextDouble();
        if(customer_type.equals("Regular"))
        {
            Customer r=new RegularCustomer(id,name,purchaseweight,goldRatePerGram);
            r.display();
        }
        else
        {
            Customer p=new PremiumCustomer(id,name,purchaseweight,goldRatePerGram); 
            p.display();
        }
        
    }
}

```

## OUTPUT:

<img width="859" height="708" alt="image" src="https://github.com/user-attachments/assets/19b24c84-60de-4c8a-9273-574089139546" />


## RESULT:
The program successfully implements inheritance to calculate gold purchase prices for regular and premium customers. Regular customers receive a 2% discount, while premium customers receive a 5% discount along with 1% cashback on the final price. The output correctly displays customer details, discount applied, final price, and cashback (for premium customers).
