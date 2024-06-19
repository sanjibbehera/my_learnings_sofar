# Tech Lingos

## Cloud Computing
- **AWS (Amazon Web Services)**: A comprehensive and widely adopted cloud platform offering over 200 fully featured services from data centers globally.
- **Azure**: Microsoft’s cloud computing platform and service, used to build, deploy, and manage applications through a global network of Microsoft-managed data centers.
- **GCP (Google Cloud Platform)**: A suite of cloud computing services that runs on the same infrastructure that Google uses internally for its end-user products.

## Communication
- **Long polling**: It is a web communication technique used to achieve real-time interaction between a client and a server. It is one of the methods employed to implement push technology, enabling the server to send updates to the client as soon as new data is available.
  - Disadvantages:
    - **Resource Intensive**: Keeping connections open for long periods can be resource-intensive for the server.
    - **Latency**: Although it provides real-time updates, there can still be some latency compared to WebSockets.
    - **Scalability**: May require careful management of server resources and tuning to handle a large number of concurrent connections efficiently.
  - UseCase:
    - **Chat Applications**: Frequently used in chat applications to provide real-time messaging between users.
    - **Notifications**: Suitable for delivering real-time notifications to clients, such as alerts, updates, or changes in status.
    - **Real-Time Data Feeds**: Can be used to push updates from servers to clients in applications like stock ticker updates, sports scores, or social media feeds.
- **WebSockets**: It is a communication protocol that provides full-duplex communication channels over a single, long-lived connection. This protocol is designed to allow web applications to maintain an open connection between the client (e.g., a web browser) and the server, enabling the real-time, bidirectional exchange of data with low latency.
  - Features:
    - **Full-Duplex Communication**: WebSockets allows both the client and server to send messages independently of each other over a single connection, enabling real-time interactivity.
    - **Persistent Connection**: Unlike traditional HTTP requests, which are stateless and require a new connection for each request/response pair, WebSockets maintain a persistent connection that can stay open as long as needed.
    - **Low Latency**: By avoiding the overhead of establishing a new connection for each message, WebSockets reduce latency and improve performance for real-time applications.
    - **Efficiency**: WebSockets use a lighter communication protocol compared to HTTP, reducing the amount of data transmitted and making it more efficient for real-time data exchange.
  - Data Flow Comparision:
    - **HTTP Data Flow**:  
    ![Alt text](Images/HTTP-Connection.png?raw=true "Title")  

    - **Websocket Data Flow**:  
    ![Alt text](Images/WebSocket-Connection.png?raw=true "Title")
- **RSockets**: It is an application layer protocol and it supports Reactive Streams semantics. It supports client-server and server-server communication.
  - **Performance**: WebSockets doesn't support multiplexing. While RSocket solves the multiplexing problem by creating many channels within a network connection. Multiplexing divides the capacity of a network connection into many logical channels. And each logical channel transfers a separate data stream. RSocket communication is asynchronous.
  - **Data Format**: RSocket uses the binary protocol on top of TCP, WebSockets, or Aeron. Put another way, it’s transport layer agnostic. An RSocket message consists of data and metadata. Yet data and metadata can be in different data formats. Besides RSocket supports RPC and event-based messaging. And sends real messages instead of just bytes.
  - **Flexibility**: RSocket is supported by most programming languages. And it offers application-level flow control. So there's no need to implement buffering or windowing on the application. Instead the consumable amount of messages can be specified.
  - **Resilience**: Each channel within an RSocket connection does backpressure independently. Put another way, there’s data flow control on each logical stream. RSocket supports keepalive heartbeat signals.

## DevOps
- **CI (Continuous Integration)**: It is the practice where developers regularly merge their code changes into a central repository, after which automated builds and tests are run.
- **CD (Continuous Delivery)**: It is a software development practice where code changes are automatically prepared for a release to production.
- **CD (Continuous Deployment)**: It is a strategy in software development where code changes to an application are released automatically into the production environment.

## Tech Stack
- **Ejabberd**: Open source real-time messaging server written in Erlang.  
- **Google Push**: 3rd Party service to provide push notifications.
- **H3 Library**: Hexagonal shaped hierarchical gepspatial indexing system created at Uber.
- **Vitess MySQL**
- **VTTablet**
- **VGate**
- **Zookeeper**
- **PgBouncer**
- 

## Infra
- **Latency**: It is the delay that happens between a user takes an action on network or web application and when they get a response.
- **Throughput**: It is the measure of how many units of information a system can process in a given amount of time.
- **Concurrency**: It is the execution of multiple instruction sequences at the same time.
- **Fault Tolerance**: It refers to the system's ability to continue operating despite failures or malfunctions.
- **Durability**: It refers to the property that ensures data is permanently stored and will not be lost or corrupted, even in the event of a system crash, power failure, or other catastrophic events. Durability is one of the four ACID properties (Atomicity, Consistency, Isolation, Durability) that define reliable transaction processing in databases.
- **Data Redundancy**: It refers to the practice of storing the same piece of data in multiple locations within a database or across different systems. While redundancy can sometimes lead to inefficiencies and increased storage costs, it is also a critical component of ensuring data availability, reliability, and fault tolerance in many computing systems.
- **Bracketing**:
- **Data Isolation**:
- **High Availability**:
- **RAID (Redundant Array of Independent Disks)**:

## Database Terms
- **Leader Follower Replication Topology**:
- **Deduplication**: It is a data compression technique used to eliminate duplicate copies of repeating data. The goal of deduplication is to reduce the amount of storage space needed to save data by ensuring that only unique instances of data are stored. Duplicate data is replaced with a reference to the single copy of the stored data, significantly optimizing storage efficiency and reducing costs.
- **Normalization**: In relational databases, normalization techniques can minimize unintentional redundancy by organizing data into related tables and eliminating duplicate information.
- **Database Replication**: Data is copied from one database server to another. This ensures data availability and reliability, especially in distributed systems.
- **Intentional Redundancy**: This is deliberately implemented to enhance data availability, reliability, and performance. Examples include RAID configurations, database replication, and backup systems.
- **Unintentional Redundancy**: This occurs due to poor database design or data management practices. Examples include duplicate records in a database or repeated data across different tables without normalization.
- **salt the passwords**: According to OWASP guidelines, “a salt is a unique, randomly generated string that is added to each password as part of the hashing process”.

## Miscellaneous
- **Reactive Systems**: A systems that are Responsive, Resilient, Elastic and Message Driven. They are are more flexible, loosely-coupled and scalable.  
  ![Alt text](Images/reactive-traits.svg?raw=true "Title")  
- **Hot Code Loading**: The aim is to update the current running code with new code without stopping the service. It is offered by **Erlang**.
- **Backpressure**: Slowing down data flow to prevent overwhelming the receiver.
- **Horizontal Scaling (aka scaling out)**: It refers to adding additional nodes or machines to your infrastructure to cope with new demands.
- **Vertical Scaling (aka scaling up)**: It describes adding additional resources to a system so that it meets demand.
- **Diagonal Scaling**: It is a hybrid of horizontal and vertical scaling.
- **Load Testing**: It is the process of measuring the performance of the system under the anticipated load.
- **WSGI (Web Server Gateway Interface)**: It is a simple calling convention for web servers to forward requests to web applications or frameworks written in the Python programming language.
- **GIL (Global Inpterpreter Lock)**: It is a mechanism used in computer-language interpreters to synchronize the execution of threads so that only one native thread (per process) can execute basic operations (such as memory allocation and reference counting) at a time. As a general rule, an interpreter that uses GIL will see only one thread to execute at a time, even if runs on a multi-core processor, although some implementations provide for CPU intensive code to release the GIL, allowing multiple threads to use multiple cores.
- **Threads V/s Processes**: Inter-thread communication (sharing data etc.) is significantly simpler to program than inter-process communication. Context switches between threads are faster than between processes. That is, it's quicker for the OS to stop one thread and start running another than do the same with two processes.  
Disadvantages:  
    - No security between threads.  
    - One thread can stomp on another thread's data.
    - If one thread blocks, all threads in task block.
- **Request Collapsing**: 
- **Request Hedging**: 
- **Request Coalescing**:


## Challenges or Problems or Bottlenecks
- **Thundering herd problem**: It occurs when a large number of processes or threads waiting for an event are awoken when that event occurs, but only one process is able to handle the event. When the processes wake up, they will each try to handle the event, but only one will win. All processes will compete for resources, possibly freezing the computer, until the herd is calmed down again.  
**Solution Video**: https://youtu.be/xrizarXJgC8
- **Shared Memory vs Private Memory**: 
  - Shared memory is a memory that may be simultaneously accessed by multiple programs or processes with the intent to provide communication among them or avoid redundant copies.
  - Private memory is memory that is exclusive to a single process. Each process has its own private memory space, isolated from other processes.
    | Characteristics | Shared Memory | Private Memory |
    |----------|----------|----------|
    | Accessibility    | Multiple processes can access the same memory space.   |  NA |
    | Communication    | Facilitates fast inter-process communication (IPC) as data can be directly shared without the need for data copying.   | NA   |
    | Synchronization    | Requires synchronization mechanisms like semaphores, mutexes, or locks to prevent race conditions and ensure data consistency.  | NA   |
    | Efficiency    | Can be more efficient in terms of memory usage and speed since data doesn’t need to be copied between processes.   | NA   |
    | Isolation    | NA   | Each process has its own separate memory space.   |
    | Security    | NA   | Provides better security as processes cannot directly access each other’s memory.   |
    | Data Protection    | NA   | Less risk of unintended data corruption since memory is not shared.   |
    | Communication    | NA   | Requires IPC mechanisms like pipes, message queues, or sockets to communicate between processes.   |
    | Use Case    | Commonly used in systems that need high-speed data sharing, such as real-time systems, databases, and multi-threaded applications.   | Suitable for applications where process isolation and security are critical, such as web servers, isolated services, and user applications.   |
  - Shared Memory Advantages:
    - Speed: Direct memory access results in faster communication between processes.
    - Resource Efficiency: Reduces the overhead of duplicating data.
  - Shared Memory Disadvantages:
    - Complexity: Requires careful synchronization to avoid issues like race conditions and deadlocks.
    - Security: Shared memory can introduce security risks if not properly managed, as unintended access or corruption of data is possible.
  - Private Memory Advantages:
    - Simplicity: Easier to manage since synchronization between processes is not required.
    - Security: Enhanced security and stability due to isolated memory spaces.
  - Private Memory Disadvantages:
    - Overhead: Inter-process communication can be slower due to the need for explicit IPC mechanisms.
    - Resource Usage: Can lead to higher memory usage as data is duplicated across processes.

- **Server Starvation**: Also known as resource starvation, occurs when a server or process is unable to obtain the necessary resources (such as CPU time, memory, or I/O bandwidth) to perform its tasks because those resources are being monopolized by other servers or processes.  
Causes:
  - High Load from Other Processes
  - Resource Contention
  - Priority Scheduling
  - Deadlock Situations
  - Improper Resource Allocation
  - Denial of Service (DoS) Attacks

- **hot sharding problem**: 
- **rainbow tables**: