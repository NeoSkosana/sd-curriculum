## **3. Information Architecture (IA)**

The application is divided into two main sections based on user roles: Cook and Customer.

### **Site Map**

This diagram shows the primary screens and their relationships as defined in the PRD.

graph TD  
    subgraph Public  
        A[Landing Page] --> B{Register/Login};  
    end

    subgraph Customer View  
        C[Home/Discovery] --> D[Kitchen Detail & Menu];  
        D --> E[Order Summary];  
    end

    subgraph Cook View  
        F[Cook Dashboard] --> G[Menu Management];  
        F --> H[Profile Management];  
        F --> I[View Orders];  
    end

    B -->|as Customer| C;  
    B -->|as Cook| F;