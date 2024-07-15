## Table of Contents
- [Data Structures](#data-structures)
- [Algorithms](#algorithms)
- [Software Architecture](#software-architecture)
- [Operating Systems](#operating-systems)
- [Computers](#computers)
- [Networking](#networking)
- [Programming Languages](#programming-languages)
- [Databases](#databases)
- [Math](#math)
- [Security](#security)

## Data Structures
> Implementations: [Here](https://github.com/derivia/algorithms)

- [X] Bitwise Operations
    - A word is a unit of data of defined size in bits that is addressable and can be moved between the processor and storage (be it non-volatile or not).
        - Usually, the word is the size of the bus, so the movement of any word can be made with only one operation between registers.
        - And, obviously, it is typically a power of 2.
    - Left shifting by n is multiplying by 2 n times and right shifting by n is dividing by 2 n times.
- [X] Arrays
    - Fixed have a fixed size n, fixed type t with size s. The size of the array is basically n * s. Each element has a index. To get an element, go to the start of the array and multiply the index by s, some simple pointer arithmetic.
    - Constant access O(1).
- [X] Linked Lists
    - Better insertion and removal compared to arrays. Just change/add pointers to other elements.
    - Not constant access, because each element points to the next, which isn't in the "same memory location".
- [X] Stacks
    - Can be either implemented with an array or queue.
    - LIFO (last-in, first-out), which is basically "stacking" management of the elements.
    - Used in undo/redo and some implementations have priority.
- [X] Queues
    - Can be either implemented with an array or queue.
    - FIFO (first-in, first-out), a queue, useful when many things come at the same time.
    - Good for resource management in servers, managing the requests on queues.
- [X] Hash tables
    - Combines some of the best things between arrays and linked-lists.
    - Basically an array of linked-lists with hashing function, good for having near constant access.
    - The linked-lists shouldn't be too big, which means the hashing function is good and the hash table array is big enough.
    - Some of the simplest and most common hashing functions uses some prime number, and at the end makes the modulo of the
      hash table size to insert the element on a linked list based on the hash function output as index.
    - The size of the hash table should be the next prime number that is at least 1.3 times bigger than the expected number of distinct keys.
    - A clever way to handle deletion on hash tables is to mark the keys as deleted, instead of "shifting" the entire linked list items after the item back.
    - A particular "alternative" could be resizing the hash table, based on its ratio of filled buckets.
        - Maybe, if ratio is bigger than 0.7 after insertion/deletion: grow to the next prime number at least twice as big than the current size.
        - And if ratio is lower than 0.7 after insertion/deletion: shrink to the next prime number at least twice as small than the current size.
- [-] @TODO: (continue) Trees
    - Non-linear data structure (doesn't have an logical start and end), hierarchically.
    - Trees consists of nodes, the first node is called root.
    - I saw somewhere that the nodes without children can be called leaves.
    - The connections between nodes are called edges.
    - Height: the longest length between a leaf and its root.
    - Depth: the length between a specific node and its root.
    - Binary tree
        - A binary tree is one that has at most two children nodes for each node.
        - The nodes are called left and right.
        - @TODO: Make a binary tree in C.
        - @TODO: Continue notes about trees.
    - @TODO: Add notes about different tree and their uses.
- [ ] Graphs

## Algorithms
> Implementations: [Here](https://github.com/derivia/algorithms)

- [X] Complexity (Big-O)
    - To avoid the difference between CPUs runtimes in seconds/minutes, Big-O notation works based on the limit concept, as n grows towards infinity, how does the algorithm behaves.
    - The most common O notations, in increasing order: O(1) < O(log n) < O(n log n) < O(n) < O(n^2) < O(2^n) < O(n!)
    - Dropping the less significant terms and constants, we use asymptotic notation.
        - As in: an^2 + bn + c
        - There will always be a moment where bn + c (starts being) < an^2.
    - [Big-O Cheat sheet](http://bigocheatsheet.com/)
- [X] Sorting (common sorting algorithms)
    - The following two are commonly considered the most efficient:
    - [X] Merge sort
    - [X] Quick sort
- [X] Searching
    - [X] Linear search
        - Works on non-ordered elements.
        - It is O(n).
    - [X] Binary search
        - Works only on ordered elements.
        - It is O(log n).

## Software Architecture

### Amazon Web Services

- A simplification of the billions of things they have: [AWS in plain english](https://expeditedsecurity.com/aws-in-plain-english)

### PaaS and IaaS

#### PaaS

- Platform as a Service
    - The client has access to the necessary execution environment for his applications.
    - The infrastructure is managed by the provider.
    - Example: Heroku.

#### IaaS

- Infrastructure as a Service
    - The client can manage the virtual machines that have the necessary components to run the application.
        - Data storage, operating systems, etc.
    - The provider manages the hardware.
    - Example: AWS EC2.

### "Evolution" of architectures

1. Monolithic
    - Tightly coupled within a single codebase.
    - Source code for different purposes on the same files.
    - Challenges: Complexity of updating and deployment.
2. Multitier
    - Separated source code by purpose.
    - e.g.: presentation, logic and data layers.
    - Challenges: Fault isolation and scalability
3. Microservices
    - Applications are composed of smaller deployable services.
    - Each service focuses on a specific business and communicates with others using APIs, typically over HTTP or messaging protocols.
    - Challenges: Data consistency and communication.

### APIs

- REST
    - Communicates through JSON, XML, HTML, etc.
    - Typically used in modern applications and public APIs.
    - Dependent on the HTTP transport protocol.
- SOAP
    - Communicates through XML.
    - Generally used in legacy applications and private APIs.
    - Independent of the transport protocol.

### Message Queuing

- Uses a message broker to pass messages between processes/systems.
- The system that uses message queuing doesn't require an immediate response to continue working.
- Achieves asynchronous communication between different components
- Instead of communicating directly with each other, components send messages to the message broker, which delivers them to the intended recipients.
- RabbitMQ
    - It acts as an intermediary between different parts of an application or between different applications in a queued manner.
    - Imagine that in a few days, a new Marvel movie scheduled to be released. Many users visit a hypothetical website, "https://movietickets.com," to reserve their tickets for the movie. However, the system does not use a queue to handle the high demand, resulting in failures.
    - Implementing a queue ensures that even under heavy loads, the application continues to respond, albeit at a slower pace.

### SOLID

- Single Responsibility
    - A class should have only one job.
- Open-Closed
    - A class/module should be open for extension but closed for modification.
- Liskov Substitution
    - Superclasses should be replaceable by its subclasses.
- Interface Segregation
    - Interfaces should be specific, avoiding the need to have unnecessary functions.
- Dependency Inversion
    - Decouple classes from implementations, using abstractions.

### Entities and DTOs

- Entities typically represent the structure of data in database (meaning they usually are 1:1 with database entities), while DTOs are used to pass information between functions on the backend, as example, if there is no need to have an user password (hashed or not) being passed around, them a user dto should be used, which should have only the necessary data.

### Docker

- What is docker
    - Docker is a way to execute project development and deployment without worrying too much with the dependencies, since everything that runs in docker is isolated from the external environment on a Container, which should have every dependency the application needs, making it easier to produce the same results on different machines.
- Images and Containers
    - Images are like templates for creating containers, for example, you can have a Docker image that contains all the required components for running certain web server.
    - Containers are instances of Docker images that run in memory, for example, you can isolate three different APIs, all managed by an Nginx web server, and they all share the same database. Each of these components can run in its own Docker container. To manage the configuration of these containers, docker compose can be used, which defines the relationships and configurations between containers in a single file.
    - Also, i think docker is good for testing the application under "low-resource conditions", like setting up on docker compose that each API should have only 275mb of ram and 1 CPU.

### Tests

- Test Driven Development
    - A approach to follow from the beginning of application development, as the name suggests, where the application is developed based on tests.
- Unit Testing
    - Conducted on small parts such as functions/methods, often using mock objects as parameters.
    - Generally, when some code is hard to test, it's an sign that the code should be improved.
        - But even if the project has a high degree of decoupling (which means it's easy to unit test), it can still be a bad implemented one.
- Integration Testing
    - Conducted on connections between different parts of the application.

### Caching

- Caching is a method to speed up responses by increasing the use of storage.
- It can be done in various ways, typically categorized as server-side and client-side caching.
- In client-side caching, it involves storing static resources that change infrequently and are frequently accessed. This reduces the demand on the web server, as the browser checks if the resource is stored in the cache before requesting it.
- In server-side caching, a database technology is often used to accelerate queries made to a parent database.
- It also plays a role in how parts of the DNS work; recently accessed websites are stored in the cache to avoid the need for repeated lookups.

### HATEOAS (Hypertext as the Engine of Application State)

- A principle in RESTful APIs that makes the API's usage self-explanatory by providing links to related operations.
- It allows the API consumer, typically a developer, to easily navigate operations, as, typically, end-users don't interact with the API JSON "directly" but rather perceives it in the formatting provided by the front-end developer.

### MVC Pattern

- Model
    - Represents the data and business logic of your application.
    - Entities like User and Post would typically be part of the model layer.
    - These entities define the structure of data and may include methods for interacting with the data.

- View
    - Handles the presentation layer.
    - In a frontend context (React), views are typically components that render UI elements based on the data provided by the controller.
    - In a backend context, views can represent templates or responses sent to clients.

- Controller
    - Acts as an intermediary between the model and the view.
    - Handles user input and updates the model or directs the view to change based on that input.
    - Receives requests and sends responses.

### @TODO: GoF Patterns

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

### @TODO: Code Review, Merge & CI/CD

## Operating Systems

### Memory Allocation

- Memory layout
    - A process runs within it's own separated memory space. Usually formed in 5 parts.
    - Text section: Binary instructions
    - Data section: Non-zero static data
    - BSS (Block Started by Symbol): Zero static data
    - Heap: Dynamically allocated data
    - Stack: Implicit variables created, function arguments, copies of pointers, etc.
    - The stack and the heap grows in opposite directions, the heap has a pointer called brk, which is the end of the heap, on the top.
    - As more memory is allocated for a process using something like new or malloc, the heap grows as brk goes up.
    - This layout applies to a single process memory, not the entire computer memory.

### Windows Processes

- Virtual address space
    - A set of memory that is mapped so the process can use without interfering with other processes memory.
- Executable program
    - The code/data that is mapped into the virtual address space.
- Security context
    - Access token that identifies user, security group, privileges, capabilities, session and other securiry-related things that are associated with the process.
- Process ID
    - The unique identifier of the process.
- Open handles list
    - Files, semaphores and other things that are accessible to the threads of the process.

### Linux Kernel

#### What the kernel is responsible for

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
- Inter-process Communication (IPC)
    - Mechanisms which allows data exchanges between threads of one or different processes.
- Syscalls
    - Low-level interfaces provided by an operating system for accessing its services. They allow programs to interact with the underlying hardware resources, such as file systems, input/output operations, process management, etc. Syscalls are generally implemented through specific function invocations from the user space to the kernel space, and they provide a standardized way for programs to request system resources and services.

## Computers

### Fetch-Decode-Execute cycle

1. Fetch
    - The CPU fetches the next instruction from memory.
    - The memory address of the instruction is stored in the Program Counter (PC).
    - The fetched instruction is stored in the Instruction Register (IR).
2. Decode
    - The CPU decodes the instruction in the IR.
    - Decoding determines what the instruction is asking the CPU to do.
3. Execute
    - The CPU performs the action required by the instruction.

- After execution, the cycle repeats with the next instruction.

## Networking

### Basics

- Network is the interconnection two different computers in order to make then communicate (exchange data), they are able to do that while following some kind of protocol.
- Firewall
    - A set of algorithms used to block incoming requests that could harm the system.
- Proxy
    - Basically a man-in-the-middle, it's useful when you are connected behind a lot of proxies (aka: proxychain), to hide your own identity.
- Load balancing
    - A technique used to manage requests coming to a server, balancing the load on separated processes (and other strategies) that are isolated from each other, preventing overloading a single process.
    - Nginx is generally used as a load balancer between before two or more servers.
- IP
    - An IP address is an identifier assigned to an device on a local network that has a unique sequence of numbers, typically in the format of four sets of numbers separated by periods, such as 192.168.1.1.
- Ports
    - Used to identify applications that speaks and/or listen for connections, an application that needs a TCP connection have an assigned port.
    - Like HTTP is normally 80 and HTTPS 443.
- Packet
    - A unit of a bigger data, that goes along with others packets.
- Router
    - A device that routes packets between networks.

### Sockets

- Sockets
    - Communication endpoints in computer networks that enable data exchange between applications on different devices or systems.
        - Generally bidirectional.
    - The communication endpoint consists of ip + port: 127.0.0.1:12345
    - The socket is bound at the port and listen, accepts/refuses connections, etc.
    - Websites HTTP requests works based on sockets between the local browser and the remote server.
    - Typical HTTP server using sockets loop:
        1. Create a listener socket.
        2. Bind the socket to an address.
        3. Listen for incoming connections on the bound address:port.
        4. Accept connections from clients, creating a socket for each one.
        5. Receive the HTTP request and determine the requested file.
        6. Open the requested file to be sent.
        7. Get file status, including file size.
        8. Send the contents of the file over the connection socket.
        9. Close file descriptor and connection socket.
- A client/server interaction example
    - Client Request (as example, HTTP GET) -> Server IP + Port (SVIP+P) -> Socket bound to SVIP+P -> Process bound to the socket -> Back-end generates a response and gives it back.
    - This means that both, client (CL) and server (SV), are, at the same time, a client and a server.
        - Which means they receive and respond to interactions from the other, using a set of protocols.
    - The server HTTP socket usually binds to port 80, preventing another process from using the same port.
    - Scalability in client/server systems is achieved through techniques like load balancing and horizontal scaling.

### TCP/UDP

- TCP is used when the content that is being shared shouldn't have problems, which means there are verifications and a slower transmission in order to have properly received data.
    - Three-way handshake
        - This is an over-simplified explanation (the syn bits are important)
        1. SYN (Synchronize Sequence Number)
            - The client wants to start a communication with the server.
        2. SYN/ACK (Acknowledgment)
            - Signifies that the server received the request.
        3. ACK
            - Client acknowledges the response of the server and the connection starts.
- UDP is an alternative to TCP, which doesn't care too much about the data integrity, being used commonly on games and audio/video real time transmission.

### OSI Model

- Divided into 7 layers, each one responsible for a specific function.
- The model is a general concept of the connection between different devices, that uses different protocols.
- On a communication between computers, requests/responses don't stricly follow the layers.
    1. Physical (RJ45, DSL, etc)
        - Bits are encoded into physical signals (current, light, radio waves) and transmitted further by wire or wirelessly.
    2. Data link (MAC, HDLC, etc)
        - Physical signals are decoded back into ones and zeros, errors are corrected.
    3. Network (IP, ICMP, etc)
        - Traffic routing, DNS queries and IP packet generation.
    4. Transport (TCP, UDP, etc)
        - Data transfer based on TCP or UDP (explained later).
    5. Session (APIs sockets, etc)
        - Responsible for opening/closing sessions.
    6. Presentation (SSH, IMAP, etc)
        - Encryption/decryption and data compression.
    7. Application (HTTP, FTP, etc)
        - Allows applications to access network services such as email forwarding.

### TCP/IP model

- When connected to the internet, a computer speaks TCP/IP, which is a protocol consisting of four layers: application, transport, internet and network access.
    - TCP/IP can be compared to the OSI Model, which is a model consisting of seven layers: application, presentation, session, transport, network, data link and physical.
    - The benefits of having a layered structure, is that each layer only does what it has to do, and, while every layer is a client to another layer, it's also a server to other, as data goes in and out.

### HTTP

- A protocol used to transfer data between a server and a client based on requests and responses.
- HTTP + SSL/TLS = HTTPS
    - An encrypted version that gives more security on the communication between the server and client.
    - SSL/TLS (Secure Socket Layer / Transport Layer Security)
        - Both are certificate-based security protocols designed to establish a trust contract between client and server.
        - SSL is the older version, while TLS is the newer and more secure one.

### Topologies

- Point-to-point
    - A direct conection between two points.
    - Something like a tin can telephone.
- Bus
    - A dedicated central "bus", commonly referred as backbone.
    - All nodes are connected to the backbone.
- Ring
    - A loop made of point-to-points.
- Star
    - A switch/hub based topology, where all nodes are connected to a central node.
    - The central node acts as a repeater of the message received from one peripheral and sends to another.
- Mesh
    - A complete graph, where all nodes points to all other nodes.

### Domain names

- Human-readable addresses of web servers.
- Consists of "levels", separated by dots.
- Levels:
    - Subdomain: www, dev, etc.
    - SDL: google, youtube, twitch, etc.
    - TLD: com, org, net, us, br, etc.

### Cross-origin Resource Sharing (CORS)

- A security mechanism that helps prevent cross-origin attacks. A server defines rules determining which external origins have access to a domain's resources.
- This is why executing JavaScript functions that fetch data from an external API, imported by an open HTML file in the browser, may fail if CORS is not configured properly.

### Server Message Block Protocol (SMB)

- A client-server protocol used to share access to files, devices, serial ports, etc.
- Basically a shared hard disk on the network.

### Telnet

- Telnet is a protocol that allows remote connection and commands execution on another machine.
- As an analogy, telnet is like http and ssh is https.

## Programming Languages

### Compilation

- Lexing: transforms source code into tokens.
- Parsing: parses tokens into an abstract syntax tree (ast).
- Semantic Analysis: constructs a symbol table and performs type checking using the ast.
- Intermediate code generation: transforms the ast into an intermediate representation (ir).
- Optimization: optimizes the intermediate representation.
- Code generation: transforms the optimized ir into assembly or machine code.
- Assembly/Linking: assembles the code into binary and links it to create the final executable.

### Java access modifiers
> these are not java inclusive concepts

- public
    - accessible from any other class.
- private
    - accessible only in the class where it's defined.
- protected
    - accessible in the package where it's defined and by superclass.
- final
    - used to declare constants (immutable variables), prevent method overriding and inheritance of classes.
- abstract
    - declare a class that cannot be instantiated and must be subclassed.
    - when used on methods, they must be implemented by subclasses.
- default
    - set when there is no access modifier explicitly set.
    - accessible in the entire package.

### Java Data Abstractions

- JDBC
    - Database-dependent API, uses raw SQL statements.
    - Used when fine-grained control over database interaction is necessary.
    - Used by Hibernate & JPA for abstracted database communication.
- JPA (Jakarta Persistence API)
    - ORM Standard specification, defines a set of interfaces that should be implemented.
- Hibernate
    - Framework for easier persistence in Java.
    - Minimizes JDBC code, providing an implementation of JPA for ORM.
- Spring Data
    - Simpliefies common database operations, allowing Repository classes to be extended.
    - The extended classes generally doesn't have the need of overrided functions, integrating easier with different databases.
- Simplifying
    - JDBC is the API used for low-level database connection and SQL request/response handling.
    - JPA is a specification which defines a set of interfaces that gives easier database operations when implemented.
    - Hibernate is a popular implementation of JPA interfaces for ORM.
    - Spring Data is itself another level of abstraction which simplifies even more, but still allows raw sql.

## Databases
> Aside from the first note, databases here usually mean "relational databases".
> And DB/db means "database".

### Basics

- Databases aren't all relational, some are noSQL: MongoDB, Redis, etc.
- SQL is the most commonly used language to speak with dbs.
- Databases are made of tables, made of rows and columns.
- Tables are unique and are used to represent separated objects/activities on the same database.
    - For example, a dvd store database could have tables called: actor, category, film, etc.
- The "relational" part comes from the fact that there are relationships created based on keys from different tables.
- Databases exists in order to have systems with large data sets that are fast, using techniques to reach ACID in most cases.
    - Sometimes ACID concepts are dropped in order to maintain performance.
- Each db has different data types, but, they usually share in common (with different names): numbers, strings, booleans and dates.
- ORM (Object Relational Mapping)
    - The concept of associating a language object with an SQL table in a one-to-one relationship, enabling the use of an object-oriented paradigm to interact with a database.

### Subsets of SQL:

- DDL (definition) - manages tables structures (creating, altering and dropping).
- DML (manipulation) - manages tables columns and rows (insertion, deletion and updating).
- DQL (query) - selects data based on specified criteria (clauses like WHERE).
- DCL (control) - manages db users access rights and permissions.
- DTL (transaction) - ensures data integrity on dbs.

### Database Design

### ACID (Atomicity, Consistency, Isolation, and Durability)

- A set of transactional standards implemented by DBMS to maintain data integrity.

### Keys

- Primary
    - A unique identifier for a row.
    - Typically an id, generally of type serial or uuid.
    - Each table typically has only one.
- Foreign
    - Used to associate a row in some table to some row on another table.
    - Makes so values are only accepted when they can reference some primary key from the other table.
    - FOREIGN KEY (fk_column_name) REFERENCES another_table_with_pk (pk_column_name)
- Relationships
    - One-to-one
        - Primary key from some table is used as both primary key and foreign key of another table.
        - e.g.: one person (from the table persons) is unique and can only have one passport (from the table passports).
    - One-to-many
        - Primary and foreign are different columns (e.g: id and book_id on a table called reviews).
            - As they are different, the foreign key is not unique.
        - The foreign key still references the primary key on the table books.
        - e.g.: one book (from the table books) is unique but can have many reviews (from the table reviews).
    - Many-to-many
        - Requires an intermediate table to establish the relationship between two other tables.
        - Primary keys from both tables involved in the relationship are stored as foreign keys in the intermediate table.
        - e.g.: an intermediate table named "user_groups" could store pairs of user IDs and group IDs to signify which users are members of which groups.
            - a user can be part of many groups and a group can have many users.

### Data modelling

- High level/abstract design phase, describing these three things:
    - Entities
        - Represents the objects (data) contained in the database, which typically become tables in a relational db.
        - e.g., students, teachers, courses.
    - Relationships
        - Represents how different entities interact with each other.
        - e.g., a student has a one-to-many relationships with both courses and teachers.
    - Constraints
        - The rules enforced to entities in order to maintain data integrity.
        - A common rule are unique identifiers (id) for each entity (student_id, teacher_id, course_id).
        - e.g., course_id in the student-course relationship must reference an existing course_id in the courses table.
        - e.g., students must be enrolled in at least two courses, each teacher must be assigned to at least one course.

### Transactions

- A sequence of various operations performed on a specific database. The goal is to adhere to the "A" in ACID (Atomicity), ensuring that when these operations occur, they happen in their entirety.

### N + 1

- A problem in which multiple queries are executed to retrieve data that could have been fetched in fewer queries.

### Normalization

- Reducing redundancy by dividing tables and establishing relationships between them.
- Splitting up data to remove duplication and improve data integrity.

## Security

### Json Web Token

- A standard popular for user authentication.
- Claims
    - Statements about an entity, as example, a claim might assert the user's identity/permissions.
- Divided in three parts:
    1. Header
        - Contains metadata, such as, token type (jwt) and signing algorithm.
    2. Payload
        - Contains the claims.
    3. Signature
        - Crytographic signature used to authenticate that the token hasn't been tampered with.
        - Created by concatenating the encoded header and payload, then signing with a private key.

### Password storing

- A hash, compared to an ciphertext (text that has been encrypted by some kind of encryption algorithm), is generated with the goal of being irreversible.
- User passwords should be hashed, always, never saved as plaintext (text has NOT been encrypted).
    - Always use hashing functions designed to store passwords: bcrypt, scrypt, argon2id.
        - These tend to be slower, which is good, slows down brute force attacks.
- The dumb thing to do is just hashing, even with a strong password hashing function, a salt should be added.
    - Salts should be big strings randomly generated (using CSPRNG(s), crypto-safe pseurandom number generator(s)), that are appended to the password before hashing.
        - Salts should be stored on the database besides the hashed password (the same that has hashed using the salt).
        - The objective of salts is to avoid lookup tables attacks, where a giant collection of pre-hashed passwords are stored.

### Encryption

- Symmetric
    - Bad, basically a password-based protection (encrypt/decrypt [lock/unlock] with the same key), if someone has the password, every other content that is locked by the same password can be decrypted.
- Asymmetric
    - Better, a key-pair is generated based on some algorithm, one public and one private.
        - Something like RSA.
    - The public key encrypts, the private key decrypts.
    - Like on WhatsApp, i encrypt my message with the public key of some contact of mine. Then, they receive it encrypted, and only their private key can decrypt the message.

### Authentication/Authorization

- Authentication
    - Confirms an user identity.
    - Is when a user wants to login. The combination of the username/email + password/passkey is handled by the server.
    - If the result of the hash (maybe with salt) is the same as the one stored on the database, the user will be logged in.
- Authorization
    - Determines actions/resources a user has permissions.
    - Is when a user wants to read/write something, if he has sufficient privileges, he is able to do so.

### Reconnaissance

- Enumeration
    - The process of gathering information on a target in order to find potential attack vectors.
    - Nmap
        - A port scanning tool that tries to communicate with each port, and, depending on the response, it tries to determine if the port is open, closed or filtered (firewall).
        - When a port is open, a service enumeration can be done. It is possible to get things like the service version.
        - Common scan types:
            - TCP (-sT)
                - If the server responds with RST after a SYN (TCP handshake), it means the port is closed.
                - Ports behind a firewall doesn't respond at all, which would be marked as filtered.
                - But, it's easy to make ports that are behind a firewall respond with RST.
                - Making it harder to differentiate when a port is closed/filtered.
            - UDP (-sU)
                - Normally there is no response, so nmap marks ports as open|filtered, then try again to send another UDP.
                - The target responds with a ICMP ping if the port is closed, then nmap marks it.
                - This is important: nmap -sU --top-ports 20
                    - UDP port scanning is usually slower than TCP ones, and there are generally no UDP ports open.
            - SYN/ACK (-sS)
                - Nmap sends a RST instead of the final ACK, making the server stop trying to establish connections.
                - Also, some systems log only "fully-finished" TCP connections, so the "non-finished" three-way handshake would not appear on their logs.
                - To send a RST, nmap needs sudo privileges, in order to create raw packets.
        - ICMP is, by default, blocked on Windows systems.

### OWASP TOP 10 vulnerabilities

- Open Web Application Security Project (OWASP) is a an organization dedicated to web applications security.
    - They have a yearly report, which is OWASP TOP 10, that outlines the 10 most critical vulnerabilities.

- XSS
    - Cross-site scripting is when an attacker injects malicious scripts to be executed by other browsers.
    - Reflected
        - Client-supplied data in HTTP is included on the HTML without validation.
    - Stored
        - Content stored on the website is not validated.
        - e.g.: a user profile bio with an script tag that is executed when the page renders.
    - DOM-Based
        - Data is taken from the URL and directly inserted into the DOM without validation.
    - Blind
        - Basically a stored XSS, but on the "server-side", things like staff contact, etc.
        - Any interface where the client is able to connect "more directly" with an authority of the website is prone to Blind XSS when not properly managed.
    - Mitigation
        - Encode HTML before rendering.
        - Implement a strict CSP (Content Security Policy), which means restrict the scripts execution sources.
        - Validate input on client and server.
- SSRF
    - Server-side request forgery is when the attacker is able to make the server make requests to unintended locations, often internal locations like system/configuration files.
    - Mitigation
        - Validate/sanitize input
        - Restrict outbound connections
