## **2. Requirements**

### **Functional Requirements**

* **FR1:** A user must be able to register as either a "Cook" or a "Customer".
* **FR2:** Cooks must be able to create and manage one "Kitchen Profile" which includes a name, location (suburb/area), and a short bio.
* **FR3:** Cooks must be able to add, edit, and delete meal items from their menu. Each meal must have a name, description, price, and an optional photo.
* **FR4:** Customers must be able to view a list of all kitchens.
* **FR5:** Customers must be able to search for kitchens by their location (suburb/area).
* **FR6:** Customers must be able to view the menu for a specific kitchen.
* **FR7:** Customers must be able to place an order from a kitchen's menu. The system shall notify the cook of the new order.
* **FR8:** Cooks must be able to view a simple list of their active orders.
* **FR9:** The system shall provide an AI-powered "Menu Description Writer" to assist cooks in creating appealing meal descriptions based on keywords.
* **FR10:** Cooks must be able to update the status of an order (e.g., from 'Pending' to 'Ready for Collection' to 'Completed').

### **Non-Functional Requirements**

* **NFR1:** The application must be mobile-first and fully responsive.
* **NFR2:** Page load times for browsing menus should be under 3 seconds on a standard 3G connection.
* **NFR3:** The user interface must be simple and intuitive, requiring minimal technical literacy.
* **NFR4:** The system must handle at least 50 concurrent users without significant performance degradation.