## 📝 Project Description

A basic inventory management system that can store and manage items in a store. The system should allow users to add new items, update existing items, view all items, and search for specific items by name.

## 📌 Requirements

1.  The system should use a collection framework to store and manage the items.
2.  The system should allow users to add new items to the inventory.
3.  The system should allow users to update existing items in the inventory.
4.  The system should allow users to view all items in the inventory.
5.  The system should allow users to search for specific items by name.

## 🚀 Steps to Implement the Project

1.  Create an Item class with the following attributes: name, description, price, and quantity.
2.  Create a Store class that contains a collection of Item objects. Use ArrayList or LinkedList to store the items.
3.  Implement a method in the Store class to add new items to the collection.
4.  Implement a method in the Store class to update existing items in the collection.
5.  Implement a method in the Store class to display all items in the collection.
6.  Implement a method in the Store class to search for items by name.

## 💻 Implementation in Eclipse IDE

Assuming that you have Eclipse IDE and Java Development Kit (JDK) installed, follow these steps to implement the project:

1.  Create a new Java project in Eclipse IDE.
2.  Create a new package in the project and name it "inventory".
3.  Create an Item class in the inventory package with the following code:

```java
package inventory;

public class Item {
    private String name;
    private String description;
    private double price;
    private int quantity;
    
    public Item(String name, String description, double price, int quantity) {
        this.name = name;
        this.description = description;
        this.price = price;
        this.quantity = quantity;
    }
    
    public String getName() {
        return name;
    }
    
    public void setName(String name) {
        this.name = name;
    }
    
    public String getDescription() {
        return description;
    }
    
    public void setDescription(String description) {
        this.description = description;
    }
    
    public double getPrice() {
        return price;
    }
    
    public void setPrice(double price) {
        this.price = price;
    }
    
    public int getQuantity() {
        return quantity;
    }
    
    public void setQuantity(int quantity) {
        this.quantity = quantity;
    }
}
```

4.  Create a Store class in the inventory package with the following code:
```java
package inventory;

import java.util.ArrayList;
import java.util.List;

public class Store {
    private List<Item> items;
    
    public Store() {
        this.items = new ArrayList<>();
    }
    
    public void addItem(Item item) {
        this.items.add(item);
    }
    
    public void updateItem(Item item) {
        int index = this.items.indexOf(item);
        if (index >= 0) {
            this.items.set(index, item);
        }
    }
    
    public void displayItems() {
        for (Item item : this.items) {
            System.out.println("Name: " + item.getName());
            System.out.println("Description: " + item.getDescription());
            System.out.println("Price: " + item.getPrice());
            System.out.println("Quantity: " + item.getQuantity());
            System.out.println();
        }
    }
    
    public Item findItemByName(String name) {
        for (Item item : this.items) {
            if (item.getName().equals(name)) {
                return item;
            }
        }
        return null;
    }
}

```
5.  Create a Main class in the inventory package with the following code:
``` java
package inventory;

public class Main {
    public static void main(String[] args) {
        Store store = new Store();
        
        // Adding items to the store
        Item item1 = new Item("Milk", "Fresh milk", 2.99, 10);
        Item item2 = new Item("Bread", "Whole wheat bread", 1.99, 20);
        Item item3 = new Item("Eggs", "Large eggs", 3.49, 30);
        store.addItem(item1);
        store.addItem(item2);
        store.addItem(item3);
        
        // Updating an item in the store
        item1.setQuantity(15);
        store.updateItem(item1);
        
        // Displaying all items in the store
        store.displayItems();
        
        // Searching for an item by name
        Item foundItem = store.findItemByName("Bread");
        if (foundItem != null) {
            System.out.println("Found item: " + foundItem.getName());
        } else {
            System.out.println("Item not found");
        }
    }
}

```

6.  Run the Main class and observe the output in the console. It should display the following output:
```java
Name: Milk
Description: Fresh milk
Price: 2.99
Quantity: 15

Name: Bread
Description: Whole wheat bread
Price: 1.99
Quantity: 20

Name: Eggs
Description: Large eggs
Price: 3.49
Quantity: 30

Found item: Bread

```
This project demonstrates the use of basic Core Java features such as classes, objects, collections, methods, and control structures to create a simple inventory management system. It also shows how these features can be used to perform common operations such as adding, updating, displaying, and searching for items in the inventory.
---
#### UML Class Diagram
UML Class Diagram: This diagram represents the classes and their relationships in a Java project. It shows the attributes and methods of each class, as well as the inheritance, association, and aggregation relationships between classes.

![UML Class Diagram](https://i.ibb.co/Tq9qLP0/uml-class-diagram.png)

---
#### UML Sequence Diagram
UML Sequence Diagram: This diagram represents the interaction between objects in a Java project. It shows the order of messages sent between objects and the lifeline of each object.
![UML Sequence Diagram](https://i.ibb.co/w0YGtx2/uml-sequence-diagram.png)

---
#### UML Activity Diagram

This diagram represents the workflow of a Java project. It shows the activities, actions, and decision points in a process, as well as the flow of control between them.


![UML Activity Diagram](https://i.ibb.co/09n75TR/uml-activity-diagram.png)

This diagram represents the main flow of the program, where the `Main` class creates a new `Store`, adds two `Item` objects to the inventory, updates one of them, retrieves two items by name, and displays all items in the inventory. You can copy and paste this code into a PlantUML editor or IDE that supports PlantUML and generate an Activity Diagram.

---
#### UML Component Diagram

This diagram represents the components of a Java project and their relationships. It shows the interfaces, dependencies, and associations between components.


![UML Component Diagram](https://i.ibb.co/dGRnsTK/uml-component-diagram.png)

---
#### UML Deployment Diagram

This diagram represents the physical deployment of a Java project. It shows the hardware and software components, as well as their connections and configurations.


![UML Component Diagram](https://i.ibb.co/j32DTGG/uml-deployment-diagram.png)

---
#### UML Package Diagram

This diagram represents the organization of packages in a Java project. It shows the relationships and dependencies between packages.


![UML Component Diagram](https://i.ibb.co/8XvvsVP/uml-package-diagram.png)
