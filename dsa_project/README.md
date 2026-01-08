# Student / Parent Contact Management System (C)

This project is a **menu-driven C program** that manages student and parent contact details using **structures and arrays**.
It allows users to **add, view, search, update, and delete** contact records.

---
## Technologies Used

* Language: **C**
* Header Files:

  * `stdio.h` → for input/output operations
  * `string.h` → for string handling

---
## Program Overview

Each contact record stores:

* Roll Number
* Student Name
* Parent Name
* Parent Mobile Number

The program uses:

* **Structures** to group related data
* **Arrays** to store multiple contacts
* **Functions** for modular programming
* **Loop & switch-case** for menu-driven interaction

---

## Step-by-Step Code Explanation

---

## Header Files and Macro Definition

```c
#include <stdio.h>
#include <string.h>
#define MAX 100
```

### Explanation:

* `stdio.h` → Enables `printf()` and `scanf()`
* `string.h` → Supports string operations
* `MAX` → Defines maximum number of contacts (100)

---

## Structure Definition

```c
struct Contact {
    int roll;
    char studentName[50];
    char parentName[50];
    char phone[15];
};
```

### Explanation:

This structure stores information for **one student contact**:

* `roll` → Student roll number
* `studentName` → Student name
* `parentName` → Parent name
* `phone` → Parent mobile number

---

## Global Variables

```c
struct Contact c[MAX];
int count = 0;
```

### Explanation:

* `c[MAX]` → Array of structures to store contacts
* `count` → Tracks the number of contacts currently stored

---

## Function Declarations

```c
void addContact();
void displayContacts();
void searchContact();
void updateContact();
void deleteContact();
```

### Explanation:

These functions perform different operations on contacts, keeping the program modular and readable.

---

## Main Function (Program Execution Starts Here)

```c
int main() {
    int choice;
```

### Explanation:

* `choice` stores the user’s menu selection

---

## Menu Display Using `do-while` Loop

```c
do {
    printf("\n--- Student / Parent Contact Management System ---\n");
    printf("1. Add Contact\n");
    printf("2. Display Contacts\n");
    printf("3. Search Contact\n");
    printf("4. Update Contact\n");
    printf("5. Delete Contact\n");
    printf("6. Exit\n");
    printf("Enter your choice: ");
    scanf("%d", &choice);
```

### Explanation:

* Displays the menu repeatedly
* Takes user input
* Loop continues until the user selects **Exit**

---

## Switch Case for Menu Selection

```c
switch(choice) {
    case 1: addContact(); break;
    case 2: displayContacts(); break;
    case 3: searchContact(); break;
    case 4: updateContact(); break;
    case 5: deleteContact(); break;
    case 6: printf("Exiting program...\n"); break;
    default: printf("Invalid choice!\n");
}
```

### Explanation:

* Calls the corresponding function based on user choice
* Handles invalid inputs

---

## Add Contact Function

```c
void addContact() {
    if (count >= MAX) {
        printf("Contact list full!\n");
        return;
    }
```

### Explanation:

* Checks if contact list is full

```c
scanf("%d", &c[count].roll);
scanf("%s", c[count].studentName);
scanf("%s", c[count].parentName);
scanf("%s", c[count].phone);
```

### Explanation:

* Takes input from the user
* Stores it in the structure array

```c
count++;
```

### Explanation:

* Increments contact count after successful insertion

---

## Display Contacts Function

```c
void displayContacts() {
    if (count == 0) {
        printf("No contacts available!\n");
        return;
    }
```

### Explanation:

* Checks if there are any contacts

```c
for (int i = 0; i < count; i++) {
```

### Explanation:

* Loops through all stored contacts and prints details

---

## Search Contact Function

```c
scanf("%d", &roll);
```

### Explanation:

* Takes roll number to search

```c
if (c[i].roll == roll)
```

### Explanation:

* Compares entered roll number with stored records
* Displays details if found

---

## Update Contact Function

```c
scanf("%d", &roll);
```

### Explanation:

* User enters roll number to update

```c
scanf("%s", c[i].studentName);
scanf("%s", c[i].parentName);
scanf("%s", c[i].phone);
```

### Explanation:

* Updates the existing contact information

---

## Delete Contact Function

```c
for (int j = i; j < count - 1; j++) {
    c[j] = c[j + 1];
}
count--;
```

### Explanation:

* Shifts all records left after deletion
* Decreases total contact count

---

## Program Termination

```c
} while(choice != 6);
```

### Explanation:

* Program runs until user selects **Exit**

---
## Example Output

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
Enter your choice: 1

Enter Roll Number: 102
Enter Student Name: Anjali
Enter Parent Name: Meena
Enter Parent Mobile Number: 9123456780
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

Roll No: 102
Student Name: Anjali
Parent Name: Meena
Mobile Number: 9123456780


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
Enter your choice: 4

Enter Roll Number to update: 101
Enter New Student Name: RahulK
Enter New Parent Name: SureshK
Enter New Mobile Number: 9998887776
Contact updated successfully!


--- Student / Parent Contact Management System ---
1. Add Contact
2. Display Contacts
3. Search Contact
4. Update Contact
5. Delete Contact
6. Exit
Enter your choice: 5

Enter Roll Number to delete: 102
Contact deleted successfully!


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
## Conclusion

This project demonstrates how to manage records in C using **structures and arrays**.
It is ideal for learning **basic data management**, **modular programming**, and **menu-based applications**.
