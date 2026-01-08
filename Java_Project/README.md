# Student / Parent Contact Management System (Java)

This is a **menu-driven Java console application** that allows users to manage student and parent contact details.
The program supports **adding, displaying, searching, updating, and deleting** contact records.

---

## Technologies & Concepts Used

* Java (Core)
* Classes & Objects
* ArrayList
* Scanner class
* Loops
* Switch-case
* Menu-driven programming

---

## Program Description

Each contact record contains:

* Student Roll Number
* Student Name
* Parent Name
* Parent Mobile Number

The program stores contact records in an **ArrayList**, allowing dynamic insertion and deletion of data.

---

## Step-by-Step Program Explanation

---

## Import Statements

```java
import java.util.ArrayList;
import java.util.Scanner;
```

### Explanation:

* `ArrayList` → Stores multiple contact records dynamically
* `Scanner` → Used to take user input from the keyboard

---

## Contact Class

```java
class Contact {
    int roll;
    String studentName;
    String parentName;
    String phone;
}
```

### Explanation:

* Represents **one student contact**
* Uses variables to store student and parent details
* Demonstrates **object-oriented programming**

---

## Main Class

```java
public class ContactManagementSystem {
```

### Explanation:

* Contains the `main()` method
* Controls program execution and menu logic

---

## Data Storage

```java
static ArrayList<Contact> contacts = new ArrayList<>();
static Scanner sc = new Scanner(System.in);
```

### Explanation:

* `contacts` → Stores all contact objects
* `Scanner` → Shared for input across methods

---

## Main Method

```java
public static void main(String[] args) {
    int choice;
```

### Explanation:

* Program execution starts here
* `choice` stores user menu selection

---

## Menu-Driven Loop

```java
do {
    System.out.println("1. Add Contact");
    System.out.println("2. Display Contacts");
    System.out.println("3. Search Contact");
    System.out.println("4. Update Contact");
    System.out.println("5. Delete Contact");
    System.out.println("6. Exit");
    choice = sc.nextInt();
```

### Explanation:

* Displays menu repeatedly
* Accepts user input
* Loop continues until user chooses Exit

---

## Switch-Case Menu Selection

```java
switch (choice) {
    case 1: addContact(); break;
    case 2: displayContacts(); break;
    case 3: searchContact(); break;
    case 4: updateContact(); break;
    case 5: deleteContact(); break;
    case 6: System.out.println("Exiting program..."); break;
    default: System.out.println("Invalid choice!");
}
```

### Explanation:

* Executes corresponding operation based on user choice

---

## Add Contact Method

```java
static void addContact() {
    Contact c = new Contact();
```

### Explanation:

* Creates a new contact object

```java
c.roll = sc.nextInt();
c.studentName = sc.next();
c.parentName = sc.next();
c.phone = sc.next();
```

### Explanation:

* Takes input from the user
* Stores data inside the object

```java
contacts.add(c);
```

### Explanation:

* Adds contact to the ArrayList

---

## Display Contacts Method

```java
static void displayContacts() {
```

### Explanation:

* Checks if the list is empty
* Displays all stored contact details

---

## Search Contact Method

```java
static void searchContact() {
```

### Explanation:

* Takes roll number as input
* Searches through the ArrayList
* Displays contact details if found

---

## Update Contact Method

```java
static void updateContact() {
```

### Explanation:

* Searches contact by roll number
* Updates student name, parent name, and phone number

---

## Delete Contact Method

```java
contacts.remove(i);
```

### Explanation:

* Deletes the selected contact
* Automatically shifts remaining records

---

## Program Termination

```java
} while (choice != 6);
```

### Explanation:

* Program continues until user chooses Exit

---

## Sample Example Output

```
--- Student / Parent Contact Management System ---
1. Add Contact
2. Display Contacts
3. Search Contact
4. Update Contact
5. Delete Contact
6. Exit
Enter your choice: 1

Enter Roll Number: 101
Enter Student Name: Rahul
Enter Parent Name: Suresh
Enter Parent Mobile Number: 9876543210
Contact added successfully!


--- Student / Parent Contact Management System ---
1. Add Contact
2. Display Contacts
3. Search Contact
4. Update Contact
5. Delete Contact
6. Exit
Enter your choice: 2

Roll No: 101
Student Name: Rahul
Parent Name: Suresh
Mobile Number: 9876543210


--- Student / Parent Contact Management System ---
1. Add Contact
2. Display Contacts
3. Search Contact
4. Update Contact
5. Delete Contact
6. Exit
Enter your choice: 3

Enter Roll Number to search: 101
Contact Found!
Student Name: Rahul
Parent Name: Suresh
Mobile Number: 9876543210


--- Student / Parent Contact Management System ---
1. Add Contact
2. Display Contacts
3. Search Contact
4. Update Contact
5. Delete Contact
6. Exit
Enter your choice: 6

Exiting program...
```
---
## Conclusion:

This Java project demonstrates how to build a menu-driven contact management system using Object-Oriented Programming.

It is ideal for beginners learning:

* Java basics

* Data storage using collections

* Real-world application structure
