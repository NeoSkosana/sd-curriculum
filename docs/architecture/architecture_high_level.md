## **2\. High-Level Architecture**

### **Technical Summary**

The system will be a monolithic backend with a REST API, serving a modern, responsive frontend application. The architecture prioritizes simplicity and low operational cost. A PostgreSQL database will handle data persistence, and a monorepo structure will be used to manage both frontend and backend code, simplifying dependency management and type sharing. The AI integration will be a single, secure backend endpoint that communicates with OpenRouter.

### **Repository Structure**

A **Monorepo** structure will be used, managed with npm workspaces. This is ideal for a solo developer or small team, as it simplifies sharing types and logic between the frontend and backend, ensuring consistency.

### **High-Level Architecture Diagram**

This diagram illustrates the main components and data flow of the system.

graph TD  
    subgraph User Device  
        A[Browser on Mobile/Desktop]  
    end

    subgraph Cloud Platform (Vercel/AWS)  
        B[Frontend: React App]  
        C[Backend: Node.js/Express REST API]  
        D[Database: PostgreSQL]  
        E[AI Service: OpenRouter API]  
    end

    A -- HTTPS --> B;  
    B -- API Calls (HTTPS) --> C;  
    C -- CRUD Operations --> D;  
    C -- API Call --> E;