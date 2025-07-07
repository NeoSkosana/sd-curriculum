## **4. Technical Assumptions**

* **Repository Structure:** Monorepo. This will simplify sharing code (e.g., types) between the frontend and backend.
* **Service Architecture:** A simple monolith REST API will be sufficient for the MVP's scope.
* **Testing:** Unit tests will be required for all backend services. Frontend component testing will be required for core UI elements.
* **AI Integration:** A single API call to OpenRouter's text generation endpoint will be used. The prompt will be constructed on the backend to protect any sensitive API keys.