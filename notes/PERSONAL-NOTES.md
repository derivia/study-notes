## Topics

- [Data Structures](#data-structures)
- [Algorithms](#algorithms)
- [Software Architecture](#software-architecture)
- [Operating Systems](#operating-systems)
- [Networking](#networking)
- [Programming Languages](#programming-languages)
- [Databases](#databases)
- [Frameworks](#frameworks)
- [Math](#math)
- [Organize these in some category](#organize-these-in-some-category)

## Data Structures
> Implementations: [Here](https://github.com/lorrito/algorithms)

- [X] Arrays
    - Fixed size n, fixed type t with size s. The size of the array is basically n * s. Each element has a index. To get an element, go to the start of the array and multiply the index by s, some simple pointer arithmetic.
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
    - The linked-lists shouldn't be too big (which means the hashing function is good and the hash table array is big enough).
    - Some of the simplest and most common hashing functions uses some prime number, and at the end makes the modulo of the
      hash table size to insert the element on a linked list based on the hash function output as index.
- [ ] Trees
- [ ] Graphs

## Algorithms
> Implementations: [Here](https://github.com/lorrito/algorithms)

- [X] Complexity (Big-O)
    - To avoid the difference between CPUs runtimes in seconds/minutes, Big-O notation works based on the limit concept, as n grows towards infinity, how does the algorithm behaves.
    - The most common O notations, in increasing order: O(1) < O(log n) < O(n log n) < O(n) < O(n^2) < O(2^n) < O(n!)
    - Dropping the less significant terms and constants, we use asymptotic notation.
        - As in: an^2 + bn + c
        - There will always be a moment where bn + c (starts being) < an^2.
    - [Big-O Cheat sheet](http://bigocheatsheet.com/)
- [-] Sorting (common sorting algorithms)
    - Not going to implement since they are horrible:
        - Bubble sort
        - Insertion sort
        - Selection sort
    - The following two are commonly considered the most efficient:
        - [X] Merge sort
        - [ ] Quick sort
- [X] Searching
    - [X] Linear search
        - Works on non-ordered elements.
        - It is O(n).
    - [X] Binary search
        - Works only on ordered elements.
        - It is O(log n).
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

- "Evolution" of architectures
    - Monolithic
        - Tightly coupled within a single codebase.
        - Source code for different purposes on the same files.
        - Challenges: Complexity of updating and deployment.
    - Multitier
        - Separated source code by purpose.
        - e.g.: presentation, logic and data layers.
        - Challenges: Fault isolation and scalability
    - Microservices
        - Applications are composed of smaller deployable services.
        - Each service focuses on a specific business and communicates with others using APIs, typically over HTTP or messaging protocols.
        - Challenges: Data consistency and communication.
- Message Queuing
    - Uses a message broker to pass messages between processes/systems.
    - The system that uses message queuing doesn't require an immediate response to continue working.
    - Achieves asynchronous communication between different components
    - Instead of communicating directly with each other, components send messages to the message broker, which delivers them to the intended recipients.

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
- OSI Model
    - Divided into 7 layers, each one responsible for a specific function.
    - On a communication between computers, requests/responses don't stricly follow the layers.
    - 1 - Physical (RJ45, DSL, etc)
        - Bits are encoded into physical signals (current, light, radio waves) and transmitted further by wire or wirelessly.
    - 2 - Data link (MAC, HDLC, etc)
        - Physical signals are decoded back into ones and zeros, errors are corrected.
    - 3 - Network (IP, ICMP, etc)
        - Traffic routing, DNS queries and IP packet generation.
    - 4 - Transport (TCP, UDP, etc)
        - Data transfer based on TCP or UDP (explained later).
    - 5 - Session (APIs sockets, etc)
        - Responsible for opening/closing sessions.
    - 6 - Presentation (SSH, IMAP, etc)
        - Encryption/decryption and data compression.
    - 7 - Application (HTTP, FTP, etc)
        - Allows applications to access network services such as email forwarding.
    - The model is a general concept of the connection between different devices, that uses different protocols.
- TCP Model
- TCP/IP
    - When connected to the internet, a computer speaks TCP/IP, which is a protocol consisting of four layers: application, transport, internet and network access.
        - TCP/IP can be compared to the OSI Model, which is a model consisting of seven layers: application, presentation, session, transport, network, data link and physical.
        - The benefits of having a layered structure, is that each layer only does what it has to do, and, while every layer is a client to another layer, it's also a server to other, as data goes in and out.
- Firewall
    - A set of algorithms used to block incoming requests that could harm the system.
- Proxy
    - Basically a man-in-the-middle, it's useful when you are connected behind a lot of proxies (aka: proxychain), to hide your own identity.
- Load balancing
    - A technique used to manage requests coming to a server, balancing the load on separated processes that are isolated from each other, preventing overloading a single process.
    - Nginx is generally used as a load balancer between before two or more servers.
- IP
    - An IP address is an identifier assigned to an device on a local network that has a unique sequence of numbers, typically in the format of four sets of numbers separated by periods, such as 192.168.1.1.
- TCP/UDP
    - TCP is used when the content that is being shared shouldn't have problems, which means there are verifications and a slower transmission in order to have properly received data.
    - UDP is an alternative to TCP, which doesn't care too much about the data integrity, being used commonly on games and audio/video real time transmission.
    - Ports
        - Used to identify applications that speaks and/or listen for connections, an application that needs a TCP connection have an assigned port.
        - Like HTTP is normally 80 and HTTPS 443.
    - Sockets
        - Communication endpoints in computer networks that enable data exchange between applications on different devices or systems.
        - The communication endpoint consists of ip + port: 127.0.0.1:12345
        - The socket is binded at the port and listen, accepts/refuses connections, etc.
        - Websites HTTP requests works based on sockets between the local browser and the remote server.
- Internet
    - The giant connection of computers from around the globe, it is a network of networks basically.
- HTTP
    - A protocol used to transfer data between a server and a client based on requests and responses.
    - HTTP + SSL/TLS = HTTPS
        - An encrypted version that gives more security on the communication between the server and client.
        - SSL/TLS (Secure Socket Layer / Transport Layer Security)
            - Both are certificate-based security protocols designed to establish a trust contract between client and server.
            - SSL is the older version, while TLS is the newer and more secure one.
- Packet
    - A unit of a bigger data, that goes along with others packets.
- Router
    - A device that routes packets between networks.
- A client/server interaction example:
    - Client Request (as example, HTTP GET) -> Server IP + Port (SVIP+P) -> Socket bound to SVIP+P -> Process bound to the socket -> Back-end generates a response and gives it back.
    - This means that both, client (CL) and server (SV), are, at the same time, a client and a server.
        - Which means they receive and respond to interactions from the other, using a set of protocols.
    - The server HTTP socket usually binds to port 80, preventing another process from using the same port.
    - Scalability in client/server systems is achieved through techniques like load balancing and horizontal scaling.
- Topologies
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
- Domain names
    - Human-readable addresses of web servers.
    - Consists of "levels", separated by dots.
    - Levels:
        - Subdomain: www, dev, etc.
        - SDL: google, youtube, twitch, etc.
        - TLD: com, org, net, us, br, etc.

## Programming Languages
> these are just some notes about some languages.

### Ruby

- Enumerable common methods:

- inject/reduce
    - perform a function on every element and accumulate the result on a single value.
    - useful for transforming arrays into different data structures.
- select/find_all
    - loop over objects and return an array for which a expression returns true
    - filtering unwanted elements.
- collect/map
    - loop over objects and add the return value to an array
    - useful when making some mathematics.
- sort
    - modifies the array by sorting it based on some comparison function.
    - useful to sort elements.

- About to_s & puts
> from launchscool.com
- "puts method calls to_s for any argument that is not an array.
    - for an array, it writes on separate lines the result of calling to_s on each element of the array."

- Ranges:
```ruby
(1..16)     # inclusive range -> 1, 2, ..., 16
(1...16)    # exclusive range -> 1, 2, ..., 15
('a'..'g')  # letters range -> a, b, ..., g
```

- Times:
```ruby
3.times do
  puts "hello, world!"
end

3.times do |iteration|   # starts from 0
  puts "iteration: #{iteration}"
end
```

- Downto & upto:
```ruby
3.upto(6) { |number| print "#{number} " }    # 3 4 5 6
6.downto(3) { |number| print "#{number} " }  # 6 5 4 3
```

### Javascript

- Closure example:
```javascript
let exampleFunction;

const closureCreateFunction = () => {
  let numberFromInside = 25;
  exampleFunction = () => {
    numberFromInside *= 2;
    console.log(numberFromInside);
  }
}

closureCreateFunction();
exampleFunction(); // 50
exampleFunction(); // 100
exampleFunction(); // 200
```

- Differents types of functions:
```javascript
// Expression
const returnSum = function (a, b) {
    return a + b;
}

// Declaration
function returnSum(a, b) {
    return a + b;
}

// Arrow
const returnSum = (a, b) => a + b;
```

- Dynamic function parameter, creating an internal array from the parameters:
```javascript
function max(...numbers) {
  let result = -Infinity;
  for (let number of numbers) {
    if (number > result) result = number;
  }
  return result;
}
console.log(max(4, 1, 9, -2));
// → 9
```

- Array destructuring:
```javascript
const names = ["maria", "lucas", "pedro", "gabriel"];
for (let [i, j] of names.entries()) console.log(`${i + 1}: ${j}`);
/*
 * 1: maria
 * 2: lucas
 * 3: pedro
 * 4: gabriel
*/

const restaurant = {
  categories: ["Vegetarian", "Italian", "Pizzeria"],
  mainMenu: ["Pizza", "Pasta", "Risotto"],
  starterMenu: ["Bruschetta", "Garlic Bread", "Caprese Salad", ["Extra-Virgin Olive Oil", "Balsamic Vinegar", "Parmesan Cheese"]],
};
const [, mainMenuFavorite] = restaurant.mainMenu; // Pasta
const [, , starterMenuFavorite, [starterMenuFavoriteCondiment]] = restaurant.starterMenu; // Caprese Salad & Extra-Virgin Olive Oil
```

- For in & For of:
```javascript
const obj = { a: 1, b: 2, c: 3 };
for (let key in obj) { // iterates over properties
  console.log(key, obj[key]);
}

const arr = [1, 2, 3];
for (let value of arr) { // iterates over values
  console.log(value);
}
```

- Array methods:
> when to use each array method

- reduce()
    - perform a function on every element and accumulate the result on a single value.
    - useful for transforming arrays into different data structures.
- slice()
    - extract a portion of the array without modifying it.
    - create shallow copy or work with a subset of the array.
- filter()
    - create a new array based on another array + conditions.
    - filtering unwanted elements.
- sort()
    - modifies the array by sorting it based on some comparison function.
    - useful to sort elements.
- map()
    - return an array of same length based on some function.
    - useful when making some mathematics.

## Databases
> Aside from the first note, databases here usually mean "relational databases".
> And DB or db means "database".

- Databases aren't all relational, some are noSQL: MongoDB, Redis, etc.
- SQL is the most commonly used language to speak with dbs.
- Databases are made of tables, made of rows and columns.
- Tables are unique and are used to represent separated objects/activities on the same database.
    - For example, a dvd store database could have tables called: actor, category, film, etc.
- The "relational" part comes from the fact that there are relationships created based on keys from different tables.
- Databases exists in order to have systems with large data sets that still are fast, using techniques to reach ACID in most cases.
    - Sometimes ACID concepts are dropped in order to maintain performance.
- When learning about dbs, it's useful to work with both self-created and samples.
- Subsets of SQL:
    - DDL (definition) - manages tables structures (creating, altering and dropping).
    - DML (manipulation) - manages tables columns and rows (insertion, deletion and updating).
    - DQL (query) - selects data based on specified criteria (clauses like WHERE).
    - DCL (control) - manages db users access rights and permissions.
    - DTL (transaction) - ensures data integrity on dbs.
- Each db has different data types, but, they usually share in common (with different names): numbers, strings, booleans and dates.
- ORM (Object Relational Mapping)
    - The concept of associating a language object with an SQL table in a one-to-one relationship, enabling the use of an object-oriented paradigm to interact with a database.
- ACID (Atomicity, Consistency, Isolation, and Durability)
    - A set of transactional standards implemented by DBMS to maintain data integrity.
- Transactions
    - A sequence of various operations performed on a specific database. The goal is to adhere to the "A" in ACID (Atomicity), ensuring that when these operations occur, they happen in their entirety.
- N + 1
    - A problem in which multiple queries are executed to retrieve data that could have been fetched in fewer queries.
- Normalization
    - Reducing redundancy by dividing tables and establishing relationships between them.
    - Splitting up data to remove duplication and improve data integrity.
- Keys
    - Primary
        - A unique identifier for a row.
        - Tipically an id, generally of type serial or uuid.
        - Each table tipically has only one.
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

## Frameworks

### Spring (Java)

- Dependency Injection
    - One way to make a component decoupled (meaning it relies on method abstractions) from something it requires is usually done through an interface. For example, a function that relies on a Set in Java could have its "concrete class" changed from HashSet to TreeSet, altering the performance and other aspects without changing its functionality because the implementations share the same methods.
    - This relationship can also be built at runtime by a inversion of control container instead of compile time and the use of DI makes unit tests easier.
- Inversion of Control with Spring
    - Spring takes the responsibility of managing various components of the application, known as Beans, which have their lifecycle and connections based on Spring's interpretation of annotations in classes/methods.
- Spring Security
    - When spring security is added to the project, the default behaviour is to only allow access to content by authenticating via username and a random password generated by spring.
    - The default username is user and the password should be random generated and printed on the console.
    - If not configured, all routes end up asking for the authentication, even routes that doesn't exist should redirect the user to /login.

### React (JavaScript)

- Components
    - Reusable pieces of UI used to create a tree of components.
- JSX
    - Declarative syntax based on JavaScript, HTML & CSS that components return.
    - Makes it easier to create components instead of writing React.createElement().
    - Transpiled by things like Babel so it can be executed.
- Props
    - Used to share data between parent and children components.
    - Range from strings to React components or JavaScript objects.
- States
    - A good way to abstract from the developer the need to keep HTML elements and JavaScript code in sync using dom manipulation.
    - The element is rendered by React every time a state is changed, updating the DOM.
- Hooks
    - Apparently all react functions that starts with "use" are hooks.
- Events
- Forms
- Redux
- Router

- A good way to render elements from a list is this syntax, using the map method
```javascript
function App() {
  return (
    <>
      {array.map((element, index) => (
        <span key={index}>{element.body}</span>
      ))}
    </>
  );
}
```

## Organize these in some category

### About SOLID

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

### Analyzing different web-projects stacks

- A stack is just the set of main components from the project backend/frontend.
- Stack acronyms are commonly used on posts by people who use JavaScript, i don't know why.
- Common ones i found on the internet:
    - These first three are JavaScript based.
    - MERN (MongoDB, Express, React & NodeJS).
    - MEAN (MongoDB, Express, Angular & NodeJS).
    - MEVN (MongoDB, Express, VueJS & NodeJS).
        - MongoDB can be changed for something like PostgreSQL if it suits better.
        - Express is commonly used, but, fastify is also good.
        - React, angular and vue all are related to the visuals of the website and they are all in javascript/typescript.
        - NodeJS is just the engine that executes the javascript code.
    - LAMP (Linux (?), Apache, MySQL & PHP).
        - This appears like something a bit older than the other ones before.
        - I don't understand why linux is listed here, maybe just to have four letters.
        - Linux is commonly used as a server-side operating system, the same for MERN, MEAN, MEVN, etc.
        - Apache/Nginx is also commonly used.
- I find it strange that MongoDB appears on the three most common ones.
    - Maybe because new programmers usually think it is "the best" database.
    - I guess if you are making small websites, you don't need to choose the best, just choose one.
    - I would use MongoDB or some other NoSQL based database when ACID is not a requirement and horizontal scalability is necessary.

### Encryption

- Symmetric
    - Bad, basically a password-based protection (encrypt/decrypt [lock/unlock] with the same key), if someone has the password, every other content that is locked by the same password can be decrypted.
- Asymmetric
    - Better, a key-pair is generated based on some algorithm, one public and one private.
        - Something like RSA.
    - The public key encrypts, the private key decrypts.
    - Like on WhatsApp, i encrypt my message with the public key of some contact of mine. Them, they receive it encrypted, and only their private key can decrypt the message.

### Docker

- What is docker
    - Docker is a way to execute project development and deployment without worrying too much with the dependencies, since everything that runs in docker is isolated from the external environment on a Container, which should have every dependency the application needs, making it easier to produce the same results on different machines.
- Images and Containers
    - Images are like templates for creating containers, for example, you can have a Docker image that contains all the required components for running certain web server.
    - Containers are instances of Docker images that run in memory, for example, you can isolate three different APIs, all managed by an Nginx web server, and they all share the same database. Each of these components can run in its own Docker container. To manage the configuration of these containers, docker compose can be used, which defines the relationships and configurations between containers in a single file.
    - Also, i think docker is good for testing the application under "low-resource conditions", like setting up on docker compose that each API should have only 275mb of ram and 1 CPU.

### Code Review, Merge & CI/CD

- @TODO: Add notes about Code Review, Merge & CI/CD

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

- @TODO: Explain GoF patterns & add code examples
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

### Math

- @TODO: Maybe work on these
    - Calculus 1-3
    - Linear Algebra
    - Probability
    - Statistics
    - Differential Equations
        - Maybe maybe maybe these:
        - Numerical Analysis
        - Game Theory
        - Combinatorics
        - Set Theory
        - Number Theory
        - Topology
        - Optimization Theory
        - Mathematical Modeling
        - Complex Analysis

### Some random notes

- @TODO: Organize random notes somewhere
- Inter-process Communication (IPC)
    - Mechanisms which allows data exchanges between threads of one or different processes.
- Syscalls
    - Low-level interfaces provided by an operating system for accessing its services. They allow programs to interact with the underlying hardware resources, such as file systems, input/output operations, process management, etc. Syscalls are generally implemented through specific function invocations from the user space to the kernel space, and they provide a standardized way for programs to request system resources and services.
- HATEOAS (Hypertext as the Engine of Application State)
    - A principle in RESTful APIs that makes the API's usage self-explanatory by providing links to related operations.
    - It allows the API consumer, typically a developer, to easily navigate operations, as, typically, end-users don't interact with the API JSON "directly" but rather perceives it in the formatting provided by the front-end developer.
- Caching
    - Caching is a method to speed up responses by increasing the use of storage.
    - It can be done in various ways, typically categorized as server-side and client-side caching.
    - In client-side caching, it involves storing static resources that change infrequently and are frequently accessed. This reduces the demand on the web server, as the browser checks if the resource is stored in the cache before requesting it.
    - In server-side caching, a database technology is often used to accelerate queries made to a parent database.
    - It also plays a role in how parts of the DNS work; recently accessed websites are stored in the cache to avoid the need for repeated lookups.
- CORS (Cross-origin Resource Sharing)
    - A security mechanism that helps prevent cross-origin attacks. A server defines rules determining which external origins have access to a domain's resources.
    - This is why executing JavaScript functions that fetch data from an external API, imported by an open HTML file in the browser, may fail if CORS is not configured properly.
- RabbitMQ
    - A message queuing service, also known as a message broker or queue manager.
    - It acts as an intermediary between different parts of an application or between different applications in a queued manner.
    - Imagine that in a few days, a new Marvel movie scheduled to be released. Many users visit a hypothetical website, "https://movietickets.com," to reserve their tickets for the movie. However, the system does not use a queue to handle the high demand, resulting in failures.
    - Implementing a queue ensures that even under heavy loads, the application continues to respond, albeit at a slower pace.
