# Lab Manual 2: Django Microservices Deployment

## Objective
This repository demonstrates a microservices architecture using Django and Docker Compose. It contains two independent services (User Service and Product Service) that expose REST-style endpoints and run simultaneously in isolated containers.

## Guide Questions & Answers

**1. How does Django support microservices development?**
  Django is typically used to build large, all-in-one websites, but it also works perfectly for microservices. Instead of setting it up to load full web pages with colors and buttons, Django can be configured to simply send and receive raw text data. By using its built-in tools, developers can easily create small, focused applications that do just one specific job without any unnecessary clutter.

**2. What advantages do containers provide for Django deployment?**
  Containers act like sealed moving boxes for code. They pack the Django application and every single tool it needs to run into one complete package. The biggest advantage is that this package will work exactly the same way on any computer, which completely prevents bugs where code works on one machine but breaks on another. Containers also keep different applications safely separated from each other and allow them to start up incredibly fast.

**3. How would you enable service-to-service communication?**
  Since microservices are completely separate, they must communicate over a network. If one service needs an answer immediately, it simply connects to the web address of the other service and requests the data directly. If a task is not urgent, a service can drop a digital message into a waiting line called a message queue, allowing the receiving service to pick it up and process it whenever it has free resources.

**4. How can this setup be scaled using Kubernetes?**
  Docker is useful for local testing, but Kubernetes is the standard tool used when an application goes live to the public. If an application suddenly receives a massive wave of users, Kubernetes automatically creates dozens of identical clones of the container to handle the heavy traffic. It acts like a traffic controller, splitting the visitors evenly among all the clones so the system does not crash, and it can instantly replace any single container that happens to break.

## Proof of Completion
Below are the screenshots of the JSON responses confirming that both independent microservices are running successfully on their respective ports:

### User Service Output
<img width="1920" height="1080" alt="Screenshot (1931)" src="https://github.com/user-attachments/assets/4fdd0d51-2d70-44c0-8cfb-acaa296a2c0e" />

### Product Service Output
<img width="1920" height="1080" alt="Screenshot (1932)" src="https://github.com/user-attachments/assets/345ef449-d1e2-440d-9f0b-c15464a0fc9b" />
