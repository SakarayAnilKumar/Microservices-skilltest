# Microservices-Task

## Overview
This document provides details on testing various services after running the `docker-compose` file. These services include User, Product, Order, and Gateway Services. Each service has its own endpoints for testing purposes.

---

## Services and Endpoints

### **User Service**
- **Base URL:** `http://localhost:3000`
- **Endpoints:**
  - **List Users:**  
    ```
    curl http://localhost:3000/users
    ```
    Or open in your browser: [http://localhost:3000/users](http://localhost:3000/users)

---

### **Product Service**
- **Base URL:** `http://localhost:3001`
- **Endpoints:**
  - **List Products:**  
    ```
    curl http://localhost:3001/products
    ```
    Or open in your browser: [http://localhost:3001/products](http://localhost:3001/products)

---

### **Order Service**
- **Base URL:** `http://localhost:3002`
- **Endpoints:**
  - **List Orders:**  
    ```
    curl http://localhost:3002/orders
    ```
    Or open in your browser: [http://localhost:3002/orders](http://localhost:3002/orders)

---

### **Gateway Service**
- **Base URL:** `http://localhost:3003/api`
- **Endpoints:**
  - **Users:**  
    ```
    curl http://localhost:3003/api/users
    ```
  - **Products:**  
    ```
    curl http://localhost:3003/api/products
    ```
  - **Orders:**  
    ```
    curl http://localhost:3003/api/orders
    ```

---

## Instructions
1. Start all services using the `docker-compose` file:
   ```
   docker-compose up
   ```

2. Once the services are running, use the above endpoints to verify the functionality.

Happy testing!

## Task-outcomes

### Docker compose output

Docker-compose output

docker-compose up -d
docker-compose up -d --build (that can build the images too)

<img width="1911" height="227" alt="image" src="https://github.com/user-attachments/assets/e19498e2-7f29-4486-8474-eebdd536c983" />

Check 4 apps are running

<img width="1916" height="257" alt="image" src="https://github.com/user-attachments/assets/b9224217-5c71-4a25-ac91-794a5dfa6e4a" />

Commands used to build images

docker build -t user-service.v1.0.0 .


### Testing snippet

Users testing

<img width="1801" height="707" alt="image" src="https://github.com/user-attachments/assets/64f4c54b-0928-4ba5-a883-1ff6ed251c7a" />

Orders testing
<img width="1800" height="677" alt="image" src="https://github.com/user-attachments/assets/9a541d97-3e85-4757-9456-f034aa11d5cc" />

Product testing
<img width="1752" height="697" alt="image" src="https://github.com/user-attachments/assets/80a6aacd-fc41-4fe5-bbc9-ca2baa7903d1" />

Gateway API testing
<img width="1800" height="745" alt="image" src="https://github.com/user-attachments/assets/04a74ff2-7c17-4a2a-a4b0-89747ff1fd65" />

### Compose down

docker-compose down
<img width="1897" height="232" alt="image" src="https://github.com/user-attachments/assets/974c9cd9-8847-46bb-857f-cc86a7f8dd1e" />

<img width="1910" height="195" alt="image" src="https://github.com/user-attachments/assets/724cfea0-329d-479c-8668-5900611e3981" />

No containers running.

### Troubleshooting

Used docker logs <containername> to find the issue as I was using npm start to run the application then I came to know to use node app.js



