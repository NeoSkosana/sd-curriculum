## **4\. Data Models**

These are the core data entities required to support the application's features.

### **User**

* **Purpose:** Stores information for both "Cook" and "Customer" roles.  
* **Attributes:**  
  * id: UUID (Primary Key)  
  * email: VARCHAR(255), UNIQUE, NOT NULL  
  * password_hash: VARCHAR(255), NOT NULL  
  * role: VARCHAR(10) ('cook' or 'customer'), NOT NULL  
  * created_at: TIMESTAMP  
* **Relationships:** A Cook User has one Kitchen.

### **Kitchen**

* **Purpose:** Represents the profile of a cook's home kitchen.  
* **Attributes:**  
  * id: UUID (Primary Key)  
  * user_id: UUID (Foreign Key to User)  
  * name: VARCHAR(255), NOT NULL  
  * location: VARCHAR(255), NOT NULL (e.g., "Sandton, Johannesburg")  
  * bio: TEXT  
  * created_at: TIMESTAMP  
* **Relationships:** Has many MenuItems. Belongs to one User.

### **MenuItem**

* **Purpose:** Represents a single meal item on a kitchen's menu.  
* **Attributes:**  
  * id: UUID (Primary Key)  
  * kitchen_id: UUID (Foreign Key to Kitchen)  
  * name: VARCHAR(255), NOT NULL  
  * description: TEXT  
  * price: DECIMAL(10, 2), NOT NULL  
  * photo_url: VARCHAR(255) (Optional)  
  * is_available: BOOLEAN, DEFAULT true  
* **Relationships:** Belongs to one Kitchen. Is part of many OrderItems.

### **Order**

* **Purpose:** Represents a customer's order from a kitchen.  
* **Attributes:**  
  * id: UUID (Primary Key)  
  * customer_id: UUID (Foreign Key to User)  
  * kitchen_id: UUID (Foreign Key to Kitchen)  
  * status: VARCHAR(20), DEFAULT 'pending' ('pending', 'ready_for_collection', 'completed')  
  * total_price: DECIMAL(10, 2)  
  * created_at: TIMESTAMP  
* **Relationships:** Has many OrderItems.

### **OrderItem**

* **Purpose:** A join table connecting an Order to a MenuItem.  
* **Attributes:**  
  * id: UUID (Primary Key)  
  * order_id: UUID (Foreign Key to Order)  
  * menu_item_id: UUID (Foreign Key to MenuItem)  
  * quantity: INTEGER, NOT NULL  
  * price_at_order: DECIMAL(10, 2)  
* **Relationships:** Belongs to one Order and one MenuItem.