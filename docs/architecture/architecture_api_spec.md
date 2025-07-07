## **5\. API Specification (REST)**

A summary of the required API endpoints.

* POST /api/auth/register - Register a new user (Cook or Customer).  
* POST /api/auth/login - Login a user.  
* POST /api/kitchens - (Cook) Create a kitchen profile.  
* PUT /api/kitchens - (Cook) Update kitchen profile.  
* GET /api/kitchens?location={suburb} - (Customer) Search for kitchens by location.  
* GET /api/kitchens/{kitchenId} - (Customer) Get details of a specific kitchen and its menu.  
* POST /api/kitchens/menu - (Cook) Add a new menu item.  
* PUT /api/kitchens/menu/{menuItemId} - (Cook) Update a menu item.  
* DELETE /api/kitchens/menu/{menuItemId} - (Cook) Delete a menu item.  
* POST /api/orders - (Customer) Place a new order.  
* GET /api/orders/my-orders - (Cook) View incoming orders.  
* PUT /api/orders/{orderId}/status - (Cook) Update the status of an order.  
* POST /api/ai/generate-description - (Cook) Generate a menu description from keywords.