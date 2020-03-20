# Assignment description

## Part 1 - Required

### The Snacks machine

Progressoft would like to deploy a new snacks machine inside its premises, the new snacks machine needs to be programmed before it operates and starts serving the employees some delightful snacks.

The process to buy a snack involves the following steps:

1- The snacks machine will start with a set of snacks and will have 0 money inside it.

2- The employee will have to insert money in the machine in order to buy a snack, He / She can insert one money unit at a time; the supported units are Quarter JD, Half JD, 1 JD, 5 JDs and 10 JDs.

3- One snack should be dropped after inserting the money.

4- The machine should only drop the desired snack if the money inserted is equal or more than its price.

5- The machine should return the change (if any) to the employee.

Fortunately, the machine specs were programmed as Units test written in java. And our job now is to implement the actual code that can run the machine.

We have 2 tasks we need to accomplish to make the code execute:

* The current code in the tests does not compile yet, so our first task is to make the code compile successfully.

* We need to implement the code that makes all the unit tests pass

 
### Project structure
 
 The project is a maven project, you can start working on the project by importing it into your favorite IDE. You can run the tests using the IDE or from the command line use `mvn clean test`.
  
 
 > Changing the Unit tests code is not allowed.


package com.progressoft.induction;
import java.math.BigDecimal;
public class Money {
BigDecimal money;
public Money(BigDecimal money){
this.money = money;
}
// public void setPrice(BigDecimal money){
// this.money = money;
// }
//
// public BigDecimal getPrice(BigDecimal money){
// return money;
// }
  
// public boolean checkPrice(double price){
// if(price != .25 && price != .5 &&price != 1&&price != 5&&price != 10)
// return true;
// return false;
// }
// public boolean new_money_with_negative_value_should_fail(){
// if(this.snackMachine.getMoneyInsideMachine().compareTo(money) < 0)
// return false;
// return true;
// }
}
Snack
package com.progressoft.induction;
public class Snack {
private double price;
SnackType snackType;
  
public Snack() {
   }

public Snack(SnackType snackType, Double price) {
       this.snackType = snackType;
       this.price = price;
   }

   public double getPrice() {
       return price;
   }
   public SnackType getName() {
       return snackType;
   }
  
}
Snack Machine
package com.progressoft.induction;
import java.math.BigDecimal;
public class SnackMachine {
private BigDecimal moneyInsideMachine;
private BigDecimal moneyInTransaction;
private double Change;
public SnackMachine(){}
public SnackMachine(BigDecimal moneyInsideMachine, BigDecimal moneyInTransaction, double Change) {
this.moneyInsideMachine = moneyInsideMachine;
this.moneyInTransaction = moneyInTransaction;
this.Change = Change;
}
public BigDecimal getMoneyInsideMachine() {
return moneyInsideMachine;
}
public void setMoneyInsideMachine(BigDecimal moneyInsideMachine) {
this.moneyInsideMachine = moneyInsideMachine;
}
public BigDecimal getMoneyInTransaction() {
return moneyInTransaction;
}
public void setMoneyInTransaction(BigDecimal moneyInTransaction) {
this.moneyInTransaction = moneyInTransaction;
}
public double getChange() {
return Change;
}
public void setChange(double Change) {
this.Change = Change;
}
SnackType
package com.progressoft.induction;
public enum SnackType {
ChewingGam,Chips,Chocklate;
}


## Part 2 - Required

Please answer the following questions with no more than 2-3 lines

1- What are Mutation Observers in JavaScript?


MutationObserver is a built-in object that observes a DOM element and fires a callback in case of changes.

We’ll first take a look at the syntax, and then explore a real-world use case, to see where such thing may be useful.



2- Explain 3 different CSS selectors.

The first CSS selector selects all div elements. The second CSS selector selects all p elements. The third CSS selector selector selects all input elements.

3- What is the difference between `SessionStorage` and `LocalStorage` in HTML5?

Local storage and Session storage are the web srorage objects. Session storage is destroyed once the user closes the browser whereas, Local storage stores data with no expiration date. The sessionStorage object is equal to the localStorage object, except that it stores the data for only one session.

## Part 3 - Optional

### Snack machine UI :

We would like to have a simple UI implemented for the snack machine, this part of the assignment is considered optional but will be a plus for considering the candidate for the position.

We provide a simple sketch for the snack machine, so we need an html page that could be used to simulate the snack machine process, linking the html page with the snack machine code is out of this task scope and we are only looking for the html implementation of the page.

HTML page requirements :

* The page should include a way to simulate inserting money in the snack machine.

* The page will display the 3 types of snacks and their quantity.

* The page should display the amount of money inside the machine.

* The page should display the money of the current transaction.

* The page should display the change in case the inserted money is bigger than the item dropped.

* The page should simulate the buy action.


the image included as a [sketch](snacks-machine.png) describes  the general guide line for the page and does not mean that we want it to look exactly like that.
