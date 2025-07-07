### **4.2. Customer Discovery & Ordering**

**Goal:** A new customer discovers a local kitchen and places their first order.

graph TD  
    A[Start on Home/Discovery Page] --> B[Enter Suburb in Search Bar];  
    B --> C[View List of Nearby Kitchens];  
    C --> D[Click on a Kitchen];  
    D --> E[View Kitchen Profile & Menu];  
    E --> F[Click 'Add to Order' on a Meal];  
    F --> G{Item Added};  
    G --> H[View Order Summary/Cart];  
    H --> I[Click 'Place Order'];  
    I --> J[Confirmation Screen with Order Details];  
    J --> K[Cook receives notification];