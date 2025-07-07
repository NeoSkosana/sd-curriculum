### **4.1. Cook Onboarding & Menu Setup**

**Goal:** A new cook registers, creates their kitchen profile, and adds their first meal to the menu.

graph TD  
    A[Start on Landing Page] --> B[Click 'Register as a Cook'];  
    B --> C[Enter Email/Password];  
    C --> D{Registration Complete};  
    D --> E[Redirect to 'Create Kitchen Profile'];  
    E --> F[Fill in Kitchen Name, Location, Bio];  
    F --> G[Save Profile];  
    G --> H[Redirect to 'Menu Management' Dashboard];  
    H --> I[Click 'Add New Meal'];  
    I --> J[Fill in Meal Name, Price, Keywords];  
    J --> K[Click 'Get AI Description'];  
    K --> L[AI Generates Description];  
    L --> M[Cook Approves/Edits Description];  
    M --> N[Upload Meal Photo (Optional)];  
    N --> O[Save Meal];  
    O --> P[Meal Appears on Menu Dashboard];