## Topics

- [Data Structures](#data-structures)
- [Algorithms](#algorithms)
- [Operating Systems](#operating-systems)
- [Networking](#networking)
- [Software Architecture](#software-architecture)
- [Frameworks](#frameworks)
- [Organize these in some category](#organize-these-in-some-category)

## Data Structures
> Implementations: [Here](https://github.com/lorrito/algorithms/tree/main/code/data-structures)

- [ ] Arrays
    - Fixed size n, fixed type t with size s. The size of the array is basically n * s. Each element has a index. To get an element, go to the start of the array and multiply the index by s, some simple pointer arithmetic.
    - Constant access O(1).
- [ ] Linked Lists
    - Better insertion and removal compared to arrays. Just change/add pointers to other elements.
    - Not constant access, because each element points to the next, which isn't in the "same memory location".
- [ ] Stacks
- [ ] Queues
- [ ] Hash tables
- [ ] Trees
- [ ] Graphs

## Algorithms
> Implementations: [Here](https://github.com/lorrito/algorithms/tree/main/code/algorithms)

- [X] Complexity (Big-O)
    - To avoid the difference between CPUs runtimes in seconds/minutes, Big-O notation works based on the limit concept, as n grows towards infinity, how does the algorithm behaves.
    - The most common O notations, in increasing order: O(1) < O(log n) < O(n log n) < O(n) < O(n^2) < O(2^n) < O(n!)
    - Add mathematical explanation @TODO
    - [Big-O Cheat sheet](http://bigocheatsheet.com/)
- [-] Sorting (common sorting algorithms)
    - Not going to implement since they are horrible:
        - Bubble sort
        - Insertion sort
        - Selection sort
    - These two i think are the best ones:
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
    - [ ] Sliding Window
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

## Software Architecture

- Microsservices @TODO
- Message Queuing @TODO
 
## Operating Systems

### Memory Allocation

- Memory layout
    - A process runs within it's own separated memory space. Usually formed in 5 parts.
    - Text section: Binary instructions
    - Data section: Non-zero static data
    - BSS (Block Started by Symbol): Zero static data
    - Heap: Dinamically allocated data
    - Stack: Implicit variables created, function arguments, copies of pointers, etc.
    - The stack and the heap grows in opposite directions, the heap has a pointer called brk, which is the end of the heap, on the top.
    - As more memory is allocated for a process using something like new or malloc, the heap grows as brk goes up.
    - This layout applies to a single process memory, not the entire computer memory.

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

- Basics
    - Network is the interconnection two different computers in order to make them communicate (exchange data), they are able to do that while following some kind of protocol.
- TCP/IP
    - When connected to the internet, a computer speaks TCP/IP, which is a protocol consisting of four layers: application, transport, internet and network access.
        - TCP/IP can be compared to the OSI Model, which is a model consisting of seven layers: application, presentation, session, transport, network, data link and physical.
        - The benefits of having a layered structure, is that each layer only does what it has to do, and, while every layer is a client to another layer, it's also a server to other, as data can goes in and out.
- Firewall
    - Firewall is a set of algorithms used to block incoming requests that could harm the system.
- Proxy
    - A proxy is a man-in-the-middle, it's useful when you are connected behind a lot of proxies (aka: proxychain), to hide your own identity.
- Load balancing
    - A technique used to manage requests coming to a server, balancing the load on separated processes that are isolated from each other, preventing overloading a single process.
    - Nginx is generally used as a load balancer between before two or more servers.
- TCP or UDP
    - TCP is used when the content that is being shared shouldn't have problems, which means there are verifications and a slower transmission in order to have properly received data.
    - UDP is an alternative to TCP, which doesn't care too much about the data integrity, being used commonly on games and audio/video real time transmission.

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

## Frameworks

### Spring Framework

- Dependency Injection
    - One way to make a component decoupled (meaning it relies on method abstractions) from something it requires is usually done through an interface. For example, a function that relies on a Set in Java could have its "concrete class" changed from HashSet to TreeSet, altering the performance and other aspects without changing its functionality because the implementations share the same methods.
    - This relationship can also be built at runtime by a inversion of control container instead of compile time and the use of DI makes unit tests easier.

### Inversion of Control with Spring

- Spring takes the responsibility of managing various components of the application, known as Beans, which have their lifecycle and connections based on Spring's interpretation of annotations in classes/methods.

### Spring Security

- Basic authentication
    - When spring security is added to the project, the default behaviour is to only allow access to content by authenticating via username and a random password generated by spring.
    - The default username is user and the password should be random generated and printed on the console.
    - If not configured, all routes end up asking for the authentication, even routes that doesn't exist should redirect the user to /login.

## Organize these in some category

### Docker

- What is docker
    - Docker is a way to execute project development and deployment without worrying too much with the dependencies, since everything that runs in docker is isolated from the external environment on a Container, which should have every dependency the application needs, making it easier to produce the same results on different machines.
- Images and Containers
    - Images are like templates for creating containers, for example, you can have a Docker image that contains all the required components for running certain web server.
    - Containers are instances of Docker images that run in memory, for example, you can isolate three different APIs, all managed by an Nginx web server, and they all share the same database. Each of these components can run in its own Docker container. To manage the configuration of these containers, docker compose can be used, which defines the relationships and configurations between containers in a single file.
    - Also, i think docker is good for testing the application under "low-resource conditions", like setting up on docker compose that each API should have only 275mb of ram and 1 CPU.

### Code Review, merge, ci/cd

- @TODO

### Tests

- Test Driven Development
    - A concept (approach) to follow from the beginning of application development, as the name suggests, where the application is developed based on tests.
- Types of Tests
    - Unit Testing: conducted on small parts such as functions/methods, often using mock objects as parameters.
    - Integration Testing: conducted on connections between different parts of the application.

### APIs

- REST
    - Communicates through JSON, XML, HTML, etc.
    - Typically used in modern applications and public APIs.
    - Dependent on the HTTP transport protocol.
- SOAP
    - Communicates through XML.
    - Generally used in legacy applications and private APIs.
    - Independent of the transport protocol.

### GoF Patterns

- @TODO
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

### Some random notes

- Syscalls
    - Low-level interfaces provided by an operating system for accessing its services. They allow programs to interact with the underlying hardware resources, such as file systems, input/output operations, process management, etc. Syscalls are generally implemented through specific function invocations from the user space to the kernel space, and they provide a standardized way for programs to request system resources and services.
- Sockets
    - Communication endpoints in computer networks that enable data exchange between applications on different devices or systems.
    - The communication endpoint consists of ip + port: 127.0.0.1:12345
    - The socket is binded at the port and listen, accepts/refuses connections, etc.
    - Websites HTTP requests works based on sockets between the local browser and the remote server.
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
