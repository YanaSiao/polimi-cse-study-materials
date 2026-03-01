© Yana Siao. Academic use only. Redistribution requires attribution.

### Modeling Distributed System 15/26

* Describe the **Service Oriented Architecture** in general and the Web Service technology as an example of its implementation.  
  * Hint: SOA → Services → Loose coupling → Service provider / consumer → Registry → Web Services → SOAP / WSDL / HTTP → Interoperability  
       
* Describe and compare **data-centered and event-based** architectural styles for distributed systems.  
  * Hint: Data-centered → Shared repository → Strong consistency → Coupling → Event-based → Publish/subscribe → Decoupling → Scalability vs predictability  
      
* Describe **mobile code** paradigms and the technologies used to implement it. Make appropriate examples. Consider Tesla/ boiler, that periodically updates the firmware of millions of products sold. Which paradigm do you adopt to roll out these updates? Which paradigm is the most complex to implement and why?  
  * Hint: Mobile code → Code on Demand → Remote Evaluation → Mobile agents → Technologies (VMs, sandboxing) → Firmware updates → Complexity & security trade-offs  
      
* Describe the various kinds of **failures** in a distributed system (the failure model). Briefly discuss how complex it is to build a correct system under the various kinds of errors.  
  * Hint: Failure model → Crash → Omission → Timing → Value → Byzantine → Fault tolerance complexity


### Communication Models 13/26

* Consider **RPC and RMI** and focus on parameter passing. After describing how parameter passing works in the two systems, explain why passing parameters by reference is problematic in RPC, how RMI addresses these difficulties, and why, vice-versa, passing by value is a problem for RMI.  
  * Hint: RPC → Marshalling → Pass-by-value → Address space separation → Reference problem → RMI → Remote object references → Stubs → Pass-by-value vs identity issues  
       
* Describe the **publish-subscribe model** of communication, then compare it with RPC focusing on the following characteristics: addressing (unicast vs multicast and implicit vs explicit), synchronicity, persistence. Finally, explain how a generic DHT can be used to implement a distributed publish-subscribe dispatching service. Which is the main limitation of this implementation approach?  
  * Hint: Publish–subscribe → Decoupling → Implicit addressing → Multicast → Asynchronous → Persistence → RPC comparison → DHT-based dispatch → Topic hashing → Bottleneck & filtering limits  
      
* Describe the **message-queuing mode**l of communication, then compare it with RPC focusing on the following characteristics: addressing(unicast vs multicast, implicit vs explicit), synchronicity, persistence.  
  * Hint: Message queue → Broker → Implicit addressing → Unicast/multicast → Asynchronous → Persistence → RPC → Explicit addressing → Synchronous → Non-persistent

* You want to implement your own **streaming library** for a video service on the Internet. Describe the specific requirements of a similar service that do not fit the characteristics of the IP protocol and the mechanisms that you could put in place to address those limitations.  
  * Hint: Video streaming requirements → IP best-effort → No loss/latency guarantees → Buffering → Adaptive bitrate → Error control (FEC/retransmission) → Congestion control → Scalability mechanisms

### Naming 13/26

* Describe the concept of **structured naming** and how a structured naming system can be implemented through a hierarchy of servers. Explain also why the same hierarchy of servers does not perform equally well in presence of flat names.  
  * Hint: Structured naming → Name components → Hierarchical namespace → Delegation → Incremental resolution → Caching → Flat names → Lack of structure → Bottlenecks  
      
* Describe and compare **Iterative and Recursive name resolution** for structures naming.  
  * Hint: Structured naming → Iterative resolution → Client-driven → Low server state → Recursive resolution → Server-driven → Load & scalability trade-offs  
      
* Compare hierarchical name resolution for **flat names** with a solution that uses a DHT. Focus on performance under various situations. Identify which one of the two solutions performs better in the various cases and why.  
  * Hint: Flat names → Hierarchical resolution → Caching & locality → Bottlenecks → DHT overlay → O(log⁡N) lookups → Load balancing & churn → Performance trade-offs


* Describe the various approaches to implement a **flat naming** system: (i) in a LAN, and (ii) on a large-scale wide-area network.  
  * Hint: Flat names → Name resolution → LAN broadcast → Centralized directory → WAN hierarchy → DHT overlay → Scalability trade-offs  
      
* Describe **attribute based naming** in general, then explain why it does not scale as efficiently as structured naming. Explain its limitations in terms of performance and how they can be reduced/overcome through the use of the “**directory information tree (DIT)**”.  
  * Hint: Attribute-based naming → Attribute–value pairs → Search-based resolution → Indexing overhead → Poor scalability → Structured naming → Hierarchical resolution → Predictable performance


* Describe and compare the various techniques you know to remove **unreferenced entities** in a distributed system.  
  * Hint: Unreferenced entities → Distributed garbage collection → Reference counting → Tracing & snapshot → Weighted references → Leasing → Cycles vs overhead → Trade-offs  
  


### Synchronisation 21/26

* Describe and compare the various approaches to synchronize **physical clocks** in a distributed system. Now suppose you have to track the source of a sound with a precision of less than 1m by correlating readings of multiple, distributed microphones. Which clock synchronization approach would you use and why (sound travels at a speed of 340m per second)?  
  * Hint: Physical clock synchronization → Network-based (Cristian, NTP) → Hierarchical scaling → Hardware-assisted (GPS, PTP) → Accuracy vs cost → Timing precision requirement → Sound localization justification


* Describe how scalar clocks can be used to implement a **totally ordered multicast communication** (clarify the assumptions for the protocol to work). Compare this solution with a solution based on a centralized server in charge of receiving messages via point-to-point links and dispatching them (via point-to-point links) to every group member. Focus your comparison on the traffic generated by the two solutions and the assumptions for the two protocols to operate correctly.  
  * Hint: Scalar clocks → Timestamped multicast → Priority queue & tie-breaking → ACKs → Total order → Traffic O(N2) → Centralized sequencer → Traffic O(N) → Assumptions & trade-offs

* Describe how **scalar clocks** can be used to **guarantee causal ordering** in a broadcast communication protocol among a set of known processes. If the set of processes might change at run time, would you still be able to obtain the same result? Motivate your answer and in case of a positive answer describe how.  
  * Hint: Happens-before → Scalar clock property → Inability to detect concurrency → Violation of causality → Dynamic membership → Need for vector/dependency tracking


* Describe the problem of **mutual exclusion** and how you could solve this problem using scalar clocks. Which properties does this protocol satisfy? Under which assumptions does it operate correctly?  
  * Hint: Safety / liveness / fairness → Centralized coordinator → Lamport scalar clocks → REQUEST / REPLY / RELEASE → Token ring → Message complexity → Assumptions & trade-offs  
      
* Describe how a **Distributed Snapshot** is taken. Clarify the assumptions you made to come to the result. Give a formal definition of a consistent cut.  
  * Hint: Global state → Chandy–Lamport → MARKER messages → Channel state → FIFO assumption → Consistent cut → Happens-before closure


* Describe **pessimistic timestamp ordering**: which problem does this protocol address? How does it work? In a system with few requests to manage per second and a large dataset to access, would you use pessimistic or optimistic timestamp ordering and why?  
  * Hint: Concurrency control → Timestamp ordering → Pessimistic approach → Global timestamps → RTS / WTS checks → Serializability → Low contention workload choice  
      
* How to detect the **Computation Termination** or a Deadlock? What are the main two methods? Compare them.  
  * Hint: Termination / deadlock → Lack of global state → Snapshot-based detection → Chandy–Lamport → Diffusing computation → Probe / ACK messages → Trade-offs  
      
* Describe the **Distributed Deadlocks**, how to detect, prevent, and solve them? (Chandy-Misra-Haas protocol)  
  * Hint: Distributed deadlock → Wait-for graph → Prevention / avoidance / detection → CMH protocol → Probe messages → Cycle detection → Recovery assumptions

### Fault Tolerance 2?/26

* Calculate the recovery line for the two diagrams below using the **rollback-dependency graph** for the first one, and the **checkpoint dependency graph** for the second one. Finally, briefly describe when we build such diagrams, how we build them, and the general goal this algorithm solves.  
  * Hint:   
    * Rollback recovery → Checkpoints → Recovery line → Orphan messages  
    * Rollback-dependency graph → Process-level dependencies → Transitive rollback  
    * Checkpoint dependency graph → Checkpoint-level dependencies → Precise recovery  
    * Failure recovery → Avoid domino effect

* In a distributed system a group of servers hold the same copy of an immutable data store. Clients contact one or more elements of the group to retrieve pieces of such data. How big must the group be to **tolerate k crashes** of servers? Describe the behaviour of clients to retrieve such data (clarify your assumptions). How would your answer change if servers exhibited a byzantine behaviour?  
  * Hint: Immutable data → Replication → Crash failures → k+1 replicas → Single-server read → Byzantine failures → Incorrect replies → 2k+1 replicas → Majority read → Higher cost  
      
* Describe the **floodset** algorithm (i.e., objective, assumptions, operation) and prove it works correctly.  
 
* Describe the various alternatives for **reliable group communication** when processes are reliable but links are not.  
  * Hint: Reliable group communication → Unreliable links → ACK-based → NACK-based → Gossip dissemination → Hierarchical recovery → Scalability vs guarantees

* Describe the concept of **virtual synchrony** in general and a possible implementation. Clarify the assumptions required for the protocol to be correct.  
  * Hint: Group communication → Views → View-consistent delivery → Membership service → View change / flush → Reliable multicast → Crash failure assumptions

### Agreement

* A travel booking system coordinates flight, hotel, and car rental reservation via separate services. A central component handles user requests and communicates with each service. The system must ensure that either **all** reservations succeed **or none** does, and that progress is guaranteed. If one service fails, the entire request should be discarded. Which protocol would you use to ensure the above requirements, assuming the orchestrator is reliable, but services may fail? Motivate your answer.  
  * Hint: Atomic commitment → Distributed transaction → Orchestrator → Two-Phase Commit → Prepare phase → Commit/Abort → Atomicity → Progress under reliable coordinator

* Describe **2PL:** which problem does it solve? How does it work? Which weakness does it present? In the presence of distributed transactions and replicated data it can be implemented in various ways: describe them.  
  * Hint: 2PL → Serializability → Growing/Shrinking phases → Locks → Deadlocks → Distributed transactions → Replicated data → Primary copy → Quorums → Fully replicated locking  
      
* Describe **3PL**: which problem does it solve? How does it work? Which weakness does it present? When should we choose 3PL over 2PL?   
  * Hint: 3PL → Serializability → Deadlock avoidance → Lock phases → Reduced concurrency → Progress guarantees → 3PL vs 2PL trade-off  
      
* Consider the **Raft** consensus protocol. Which problem does it solve? Under which assumptions? Does the protocol guarantee safety (it is always correct) and liveness (it always makes progress)? Motivate your answers.  
  * Hint: Latency \- Consensus Round (Linearizability) \- Majority Quorum \- SPOF/ Fault tolerance \- Availability \- Leader Election \- Safety/ Liveness guarantees  
      
* Consider a simple **data store** and two implementations: (a) the system is implemented using a single machine, (b) the system is replicated across 5 machines using the **Raft** consensus protocol to provide consistency across replicas. Compare the two implementations in terms of response time for client requests, replication consistency, fault-tolerance.  

### Replication

* Describe the strategies and algorithms for propagating updates among a set of distributed replicas.  
      
* Describe and compare **FIFO, causal, and sequential** consistency models.  
  * Hint: Consistency models → FIFO → Program order → Causal → Happened-before → Vector clocks → Sequential → Global total order → Trade-offs  
      
* You are implementing an application where multiple processes access a replicated data store. The application requires **FIFO consistency**, but the data store you are using provides an eventual consistency model. Assuming there are no failures, does the data store satisfy the application’s requirements? If not, can you implement a mechanism to ensure FIFO consistency on top of the eventually consistent data store? How?  
  * Hint: Eventual consistency → No ordering guarantees → FIFO requirement → Per-writer order → Sequence numbers → Buffering → FIFO consistency ensured

### Data Processing

* Consider the **dataflow model** for big data processing. (a) Describe the key characteristics of the model. (b) Describe what are the two architectures to implement it: scheduling of tasks and pipelining of tasks, explain if and how they can be adopted in the case of stream processing problems. (c) compare the two approaches in terms of latency and load balancing.  
  * Hint: Dataflow model → Operators & streams → Implicit parallelism → Task scheduling → Batch / micro-batch → Higher latency → Task pipelining → Concurrent operators → Stream processing

* A social network stores a large database of photos tagged with people appearing in them. Each entry in the dataset is a pair \<p, tags\>, where p is a photo and  tags is the list of people tagged in that photo. Show using **pseudocode** how the MapReduce programming paradigm can be used to compute, for each person, the number of photos that person is tagged in.   
  * Hint: MapReduce → Map emit → Key \= person → Value \= 1 → Shuffle & group → Reduce sum → Photos per person

### P2P

* Describe the routing mechanisms of **Freenet** and **Chord** (the version with finger tables), and compare them.  
  * Hint: Freenet → Unstructured P2P → Heuristic routing → TTL → No guarantees → Chord → Structured P2P → Consistent hashing → Finger tables → O(log N) routing  
    

