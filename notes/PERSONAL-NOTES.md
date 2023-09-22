# Table of Contents

- [Computer Science](#computer-science)
  * [Data Structures and Algorithms](#data-structures-and-algorithms)
    + [Data Structures](#data-structures)
    + [Algorithms](#algorithms)
  * [Operating Systems](#operating-systems)
    + [Virtualization](#virtualization)
  * [Networking](#networking)
- [Frameworks](#frameworks)
  * [Spring Framework](#spring-framework)
    + [Dependency Injection](#dependency-injection)
    + [Inversion of Control with Spring](#inversion-of-control-with-spring)
    + [Spring Security](#spring-security)
  * [React](#react)
    + [Bootstrapping a react project](#bootstrapping-a-react-project)
    + [Components](#components)
    + [Hooks](#hooks)
    + [Props](#props)
- [Software Architecture](#software-architecture)
  * [Clean Architecture](#clean-architecture)
  * [Model View Controller (MVC)](#model-view-controller-(mvc))
- [Side notes](#side-notes)
  * [Firewall](#firewall)
  * [Proxy](#proxy)
  * [Load Balancer](#load-balancer)
  * [Docker](#docker)
  * [CI/CD](#cicd)
  * [Tests](#tests)
  * [APIs](#apis)
  * [Databases](#databases)
  * [GoF Patterns](#gof-patterns)

# Computer Science

## Data Structures and Algorithms
> Based on the following book(s): Algorithms - 4th edition and Introduction to Algorithms - 4th edition

> Every data structure and algorithm here will have an C code related to them before being marked as complete. See my [data structures and algorithms repository](https://github.com/lorrito/algorithms)

### Data Structures
- [ ] Contents to cover
  - [ ] Arrays
  - [ ] Linked Lists
  - [ ] Stacks
  - [ ] Queues
  - [ ] Hash tables
  - [ ] Trees (Binary Trees, Binary Search Trees)
  - [ ] Graphs

- Array
  - Fixed-size, same type.
  - A vector, as it is called, a dynamic-size array generally is implemented by fixing a specific size based on powers of 2.
  - I think that the efficiency of using arrays comes from the fact that the same type has the same size in memory, so to access/retrieve, it's just a simple multiplication.
  - Allowing different types, like JavaScript, as example, would have to use hashes and some different math (which i think it's a bigger processing comsumption).
- Linked List
  - More flexible
  - Single linked list (points only towards).
  - Double linked list (points towards and backwards).
  - Occupies more space in order to facilitate insert/removal.
  - Slower access/retrieve compared to arrays, but easier element adding.
- Hash tables
  - Efficient for fast data retrieval using key-value pairs.
  - Utilizes a hash function to map keys to indices.

### Algorithms
- [ ] Contents to cover
  - [ ] Sorting
    - [ ] Bubble sort
    - [ ] Insertion sort
    - [ ] Selection sort
    - [ ] Merge sort
    - [ ] Quick sort
  - [ ] Searching
    - [ ] Linear search
    - [ ] Binary search
  - [ ] Dynamic Programming
    - [ ] Fibonacci series
    - [ ] Longest Common Subsequence
    - [ ] Knapsack problem
  - [ ] Greedy Algorithms
    - [ ] Activity selection problem
    - [ ] Huffman coding
  - [ ] Graph Algorithms
    - [ ] Breadth-First Search (BFS)
    - [ ] Depth-First Search (DFS)
    - [ ] Shortest path algorithms (Dijkstra's, Bellman-Ford)
    - [ ] Minimum Spanning Tree (Prim's, Kruskal's)
  - [ ] String Algorithms
    - [ ] Pattern matching (Naive, KMP, Rabin-Karp)
    - [ ] Longest Common Substring
  - [ ] Advanced Topics
    - [ ] Divide and Conquer
    - [ ] Backtracking
    - [ ] Randomized Algorithms
    - [ ] NP-completeness and P vs NP
  - [ ] Machine Learning Algorithms
    - [ ] Linear Regression
    - [ ] Decision Trees
    - [ ] k-Nearest Neighbors (kNN)
    - [ ] Support Vector Machines (SVM)
    - [ ] Neural Networks
  - [ ] Miscellaneous
    - [ ] Bit manipulation
    - [ ] Topological sorting
    - [ ] Trie data structure
    - [ ] Segment Tree

> Practice on platforms like LeetCode, Hackerrank, etc.

## Operating Systems
> Based on the following book(s): Operating Systems: Three Easy Pieces and The Linux Programming Interface

### Linux Kernel

- What the kernel is responsible
  - Process Scheduling
    - The kernel manages the time and the resources used by processes that are residing on memory, to give the user the feeling of multitasking - each process is "processed" some fraction of second.
  - Memory Management
    - Linux employs virtual memory - each process thinks that it is using 100% of the available RAM on the computer - isolating the process from others.
    - When swap is configured, it is not necessary to let the process reside entirely on ram memory, some parts can be moved to the hard drive, which is slower, but when done properly, facilitates and allows more processes on memory, mostly the ones that consumes more memory.
  - External devices access
    - Provides a standartized interface for mices, monitors, keyboards, etc. In order to make it easier to communicate with the system.
  - Networking
    - The kernel manages processes responsible for receiving packets and routing them.
  - Provides a system call API
    - Processes are able to communicate with the kernel to perform tasks using entry points called system calls.

### Virtualization

- It's the job of the operating system to manage and concurrently execute the programs instructions by making use of its standard library of APIs (interfaces that the system calls can use in order to proper interaction and usage of the system hardware to achieve proper execution of instructions)
- The instructions of the program running are (in conjunction with the data structures that the program works on top) allocated on the memory. Which is basically an array with addresses.
  - When some instruction is called (by it address), if it writes/updates something on the memory, it should "receive" the address to write/update and the content itself.
- A process, which can be seen as the conjunction of the instructions and data that an unique program that the operating system operates (of course), has an unique PID.
  - This PID can be useful to many purposes, like interfacing to the user access to a program by abstracting from it the memory address (and other things).
    - A common use of a PID is a sigkill, which is an signal used in unix-like systems to terminate a process.
- An unique process only sees itself on the system, it sees a virtual memory that the system allocates to it in order to prevent different processes from interfering with the memory of other processes, achieving a degree of stability.
  - So two programs that allocate memory and prints the allocated memory address can have the same output, but in fact they have different memory addresses, the program is just printing what he sees, the virtual memory address from a bigger virtual memory that the system gave, from a bigger physical memory.

## Networking

- Network is the interconnection two different computers in order to make them communicate (exchange data), they are able to do that while following some kind of protocol.
- When connected to the internet, a computer speaks TCP/IP, which is a protocol consisting of four layers: application, transport, internet and network access.
  - TCP/IP can be compared to the OSI Model, which is a model consisting of seven layers: application, presentation, session, transport, network, data link and physical.
  - The benefits of having a layered structure, is that each layer only does what it has to do, and, while every layer is a client to another layer, it's also a server to other, as data can goes in and out.

# Frameworks

## Spring Framework

### Dependency Injection

- One way to make a component decoupled (meaning it relies on method abstractions) from something it requires is usually done through an interface. For example, a function that relies on a Set in Java could have its "concrete class" changed from HashSet to TreeSet, altering the performance and other aspects without changing its functionality because the implementations share the same methods.
- This relationship can also be built at runtime by a inversion of control container instead of compile time and the use of DI makes unit tests easier.

### Inversion of Control with Spring

- Spring takes the responsibility of managing various components of the application, known as Beans, which have their lifecycle and connections based on Spring's interpretation of annotations in classes/methods.

### Spring Security

- Basic authentication
  - When spring security is added to the project, the default behaviour is to only allow access to content by authenticating via username and a random password generated by spring.
  - The default username is user and the password should be random generated and printed on the console.
  - If not configured, all routes end up asking for the authentication, even routes that doesn't exist should redirect the user to /login.

## React
> Based on [Full Modern React Tutorial - Net Ninja](https://www.youtube.com/playlist?list=PL4cUxeGkcC9gZD-Tvwfod2gaISzfRiP9d)

### Bootstrapping a react project

- Vite or create-react-app
  - Vite is modern, utilizing javascript modules by default (i think) and has a faster experience, so it's what i'm going to use to bootstrap the front-end part.

### Components

- "React components are JavaScript functions that return markup"
- Basically reusable pieces of HTML

### Hooks

- Hooks are a way of keeping updated the HTML elements value at every time the page is re-rendered, among other things.
- The hook useEffect seems to be an to-go when data should be updated in order to keep the rendered components state corrects, such as fetching data from some api, updating something in intervals, etc.

### Props

- "React components use props to communicate with each other."
- It's what you should use to pass data between elements, this data can also be functions.

# Software Architecture

## Clean Architecture

- Divided into layers to ensure the protection of business rules.
- Entities: The innermost layer, representing the simplest classes that reflect business concepts.
- Use Cases: Responsible for implementing business rules.
- Interface: Acts as a bridge for use cases (business rules) to interact with entities.
- Framework and Drivers: This is where third-party components reside, such as Spring Web, Spring JPA, and MySQL/PostgreSQL drivers.

## Model View Controller (MVC)

- Model
  - The business logic, operation management, and rules.
- Controller
  - The interface between the visual elements and the model.
- View
  - The visual representation of the application.

# Side notes

## Firewall
- **TODO:**

## Proxy
- **TODO:**

## Load Balancer
- **TODO:**

## Docker

- What is docker
  - Docker is a way to execute project development and deployment without worrying too much with the dependencies, since everything that runs in docker is isolated from the external environment on a Container, which should have every dependency the application needs, making it easier to produce the same results on different machines.
- Images and Containers
  - Images are like templates for creating containers, for example, you can have a Docker image that contains all the required components for running certain web server.
  - Containers are instances of Docker images that run in memory, for example, you can isolate three different APIs, all managed by an Nginx web server, and they all share the same database. Each of these components can run in its own Docker container. To manage the configuration of these containers, docker compose can be used, which defines the relationships and configurations between containers in a single file.
  - Also, i think docker is good for testing the application under "low-resource conditions", like setting up on docker compose that each API should have only 275mb of ram and 1 CPU.

## CI/CD
- **TODO:**

## Tests

- Test Driven Development
  - A concept (approach) to follow from the beginning of application development, as the name suggests, where the application is developed based on tests.
- Types of Tests
  - Unit Testing
    - Conducted on small parts such as functions/methods, often using mock objects as parameters.
  - Integration Testing
    - Conducted on connections between different parts of the application.

## APIs

- REST
  - Communicates through JSON, XML, HTML, etc.
  - Typically used in modern applications and public APIs.
  - Dependent on the HTTP transport protocol.
- SOAP
  - Communicates through XML.
  - Generally used in legacy applications and private APIs.
  - Independent of the transport protocol.

## Databases

- ORM (Object Relational Mapping)
  - The concept of associating a language object with an SQL table in a one-to-one relationship, enabling the use of an object-oriented paradigm to interact with a database.
- ACID (Atomicity, Consistency, Isolation, and Durability)
  - A set of transactional standards implemented by DBMS to maintain data integrity.
- Transactions
  - A sequence of various operations performed on a specific database. The goal is to adhere to the "A" in ACID (Atomicity), ensuring that when these operations occur, they happen in their entirety.
- N + 1
  - A problem in which multiple queries are executed to retrieve data that could have been fetched in fewer queries.
- Normalization
  - Reducing redundancy by dividing tables and establishing relationships between them. From a design perspective, this may seem advantageous, but as I understand it, it can affect performance (resulting in a significant increase in the number of joins).

## GoF Patterns

- Creational Design Patterns
  - Abstract Factory
  - Builder
  - Factory Method
  - Prototype
  - Singleton
- Structural Design Patterns
  - Adapter
  - Bridge
  - Composite
  - Decorator
  - Facade
  - Flyweight
  - Proxy
- Behavior Design Patterns
  - Chain of Responsibility
  - Command
  - Interpreter
  - Iterator
  - Mediator
  - Memento
  - Observer
  - State
  - Strategy
  - Template Method
  - Visitor

- HATEOAS (Hypertext as the Engine of Application State)
  - A principle in RESTful APIs that makes the API's usage self-explanatory by providing links to related operations.
  - It allows the API consumer, typically a developer, to easily navigate operations, as the average client doesn't interact with the API JSON "directly" but rather perceives it in the formatting provided by the front-end developer.
- Caching
  - Caching is a method to speed up responses by increasing the use of storage.
  - It can be done in various ways, typically categorized as server-side and client-side caching.
  - In client-side caching, it involves storing static resources that change infrequently and are frequently accessed. This reduces the demand on the web server, as the browser checks if the resource is stored in the cache before requesting it.
  - In server-side caching, a database technology is often used to accelerate queries made to a parent database.
  - It also plays a role in how parts of the DNS work; recently opened websites are stored in the cache to avoid the need for repeated lookups.
- CORS (Cross-origin Resource Sharing)
  - A security mechanism that helps prevent cross-origin attacks. A server defines rules determining which external origins have access to a domain's resources.
  - This is why executing JavaScript functions that fetch data from an external API, imported by an open HTML file in the browser, may fail if CORS is not configured properly.
- SSL/TLS (Secure Socket Layer / Transport Layer Security)
  - Both are certificate-based security protocols designed to establish a trust contract between client and server.
  - SSL is the older version, while TLS is the newer and more secure one.
- RabbitMQ
  - A message queuing service, also known as a message broker or queue manager.
  - It acts as an intermediary between different parts of an application or between different applications in a queued manner.
  - Imagine that in a few days, a new Marvel movie is set to be released. Many users visit a hypothetical website, "https://movietickets.com," to reserve their tickets for the movie. However, the system does not use a queue to handle the high demand, resulting in failures.
  - Implementing a queue ensures that even under heavy loads, the application continues to respond, albeit at a slower pace.
- Nginx
  - Generally it's used for load balancing and proxies.
