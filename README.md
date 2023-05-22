[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/ZL2e6lYH)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11093602&assignment_repo_type=AssignmentRepo)

# INFO 443 Project 2 - Nodejs

Collaborators: Leah Jia, Hamda Hassan, Yuhang Liu, Efra Ahsan

## Content and Background
**Forked repo: https://github.com/efra-tech/node**   

Node.js is a popular open-source JavaScript runtime environment that can run on various platforms such as Windows, MacOSX, Linux, and more–and it’s free. It essentially enables developers to run JavaScript code on the server-side, rather than through just the web browser. Node can communicate with the computer’s server and file system in a memory-efficient, asynchronous, and single-threaded manner, which was more difficult and slow before its invention. It’s commonly used by developers to create a database within a computer’s server, and modify or use the data in a streamlined way, which therefore helps make webpage content more dynamic and pertaining to the real-time data. It provides an event-driven, non-blocking I/O model that is well-suited for building real-time and scalable network applications. Node.js is a powerful development tool for building backended web applications and has gained widespread adoption among developers.  

Node.js was written initially by Ryan Dahl, a software engineer, in 2009. He released the first version of Node.js in 2010, which initially supported only Linux and Mac OS X. Also in 2010, the Node.js environment adopted its package manager, npm, which is still in place today. The package manager streamlines the software installations and updates, as well as facilitates the ability to share and publish source code. By 2015, Node.js was governed by the Node.js Foundation, which is a collaborative project of the Linux Foundation. It has now merged with the JS Foundation to form the [OpenJS Foundation](https://openjsf.org/).   

The Node.js project has a technical steering committee (TSC) that is responsible for approving high-level changes to the codebase and architecture. The TSC is made up of a group of individuals who have made significant contributions to the project and who are elected by the community. They are responsible for voting to set the technical direction of the project and reviewing and approving changes to the codebase. In addition to the TSC, there is also a core team of maintainers who are responsible for reviewing and merging pull requests, managing issues, and ensuring the overall health of the project.   

To view the project on GitHub, navigate [here](https://github.com/nodejs/node).

To download the environment or learn more about it, navigate to their website [here](https://nodejs.org/en).

To find information on more projects governed by the OpenJS Foundation, check out their webpage [here](https://openjsf.org/projects/).

## Development View
### Overview of the Architectural Components
### System Components
#### V8 JavaScript Engine 
#### Node.js API
#### Modules
#### Web Server Application
#### Event Loop 
#### Thread Pool
#### Requests
#### Event Queue

### Organization & Interaction of Components
[include figure here]
### System Dependencies [dependencies within and without system]
### Codeline’s Model’s source code structure
### System’s approach to testing and configuration 

## Applied Perspective
The performance perspective refers to the architectural consideration of optimizing and enhancing the system’s efficiency, responsiveness, throughput, scalability, and resource utilization. This perspective aims to ensure that the Node.js system operates at its maximum potential, delivering fast and scalable performance to handle increasing workloads.

In Node.js, some of the most relevant concerns include response time, throughput, and scalability. In terms of response time, there are two classes to consider: responsiveness, which considers how quickly the system responds to routine workloads such as interactive user requests, and turnaround time, which is the time taken to complete (turn around) larger tasks. Node.js’s event-driven model is specifically designed to optimize responsiveness. By utilizing asynchronous operations, callbacks, promises, or async/await patterns, we can ensure that the system can handle multiple requests concurrently without blocking the execution. This allows the system to quickly respond to incoming requests, reducing latency and improving the overall response time.

The concern for throughput and scalability in a Node.js software system revolves around its ability to handle a high volume of requests efficiently. Node.js supports horizontal scalability, which adds more instances as the demand grows. This scalability approach ensures that the system can maintain optimal performance even under heavy loads, as the workload is distributed across multiple resources. Additionally, load balancing is significantly useful in improving the performance of the system through techniques such as round-robin, weighted distribution, and intelligent routing. Using these techniques, incoming requests can be evenly distributed among the available instances or workers, enhancing the performance of the Node system.

### Performance activities
#### Activity 1: Analyzing Throughput and Response Time
*Objective: to analyze and measure the throughput and response time of the Node.js software system to assess its performance.*
- Simulate a workload for a typical environment by conducting load tests on the system. Vary the number of concurrent users or requests to observe the system’s behavior under different loads.
- Capture and analyze the system’s ability to handle a high volume of requests. Measure the number of requests processed per second during peak load and observe any throughput bottlenecks.
- Measure the average and peak response times for different types of requests. Identify any patterns in the response time and determine whether it meets the desired performance goals.
- Analyze the collected performance data to identify potential performance bottlenecks. Look for times when the system experiences long response times or low throughput.

#### Activity 2: Load Testing and Scalability Assessment
*Objective:  to assess the scalability of the Node.js system by performing load testing and analyzing its performance under increasing workloads.*
- Run the load tests with increasing workloads to evaluate the system’s performance and scalability. Gradually increase the number of concurrent users, request rates, or data volumes
- Evaluate how the load balancing mechanism handles instances or workers that become unavailable or experience failures.
- Identify any performance limitations as the load increases and look for indicators such as response time degradation and increased error rates
- Identify any scalability constraints within the Node.js system. Evaluate components such as the web server, application server, database, or external dependencies

## Identifying Styles & Patterns Used

####  Architecture Style:

One of the architecture styles we noticed from NodeJS source code is event-driven architecture. With event-driven architecture, NodeJs can handle I/O operations efficiently.

Besides, NodeJs is a modular architecture. In the NodeJS dep folder, there are many utilized modules and dependencies like libuv, which is a library that can do asynchronous I/O. The overall architecture of NodeJS is separated into multiple modules.

#### Design patterns: 

- Event Emitter Pattern: The Event Emitter pattern is a key component of Node.js, enabling event-driven programming. The EventEmitter class is utilized to emit events, and event listeners are registered to respond to those events asynchronously. This pattern facilitates communication and coordination between different parts of the application.

- Promise Pattern:While not originally part of Node.js, Promises are widely used in modern Node.js applications and modules. Promises provide a structured and composable way to handle asynchronous operations, improving code readability and maintainability.

- OOP Pattern:

- Module Pattern:


## Architectural Assessment
- Node.js adheres to the single responsibility principle to an extent. Although node does not enforce the (SRP) principle, it does encourage developers to create small and concise modules that are responsible for one actor. For example, it’s possible for developers to have modules or classes that only focus on handling HTTP requests in a Node.js application. 
- The Open-closed design principle states that “Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification” (Thorben, 2018). Node.js does not enforce this principle so it becomes the responsibility of the developer to either include this principle or leave it. Node.js allows developers to implement the Open-closed principle. JavaScript is a flexible language and developers can use that to their advantage to build onto existing applications without modifying existing code.
- The dependency inversion principle states that “High-level modules, which provide complex logic, should be easily reusable and unaffected by changes in low-level modules, which provide utility features” (Thorben, 2018).  This principle is important as it allows developers to create classes that are easier to test. By following this principle developers can write unit tests better and increase test coverage, which then improves the overall reliability of the code. This principle also allows developers to incorporate flexibility and reusability into their applications. Node.js does not enforce the dependency inversion principle, but it allows developers to implement this principle if they want.

### Single responsibility principle

### Open-closed principle

### Dependency inversion principle

## System Improvements