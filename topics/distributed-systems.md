<h1 align="center">
Distributed systems
</h1>

### 1.  Synchronous communication how and when should be used?
<details>
    <summary>
        Answer
    </summary> 
  dadada.
</details>

### 2.  When using distributed transactions, how to keep transactions atomic (using 2PC or Sagas)?
<details>
    <summary>
        Answer
    </summary> 
 microservice-based systems. Otherwise, there is no way to tell if a transaction has completed successfully. The following two patterns can resolve the problem:
2pc (two-phase commit)
    - 2pc has two phases: A prepare phase and a commit phase. In the prepare phase, all microservices will be asked to prepare for some data change that could be done atomically. Once all microservices are prepared, the commit phase will ask all the microservices to make the actual changes.

Normally, there needs to be a global coordinator to maintain the lifecycle of the transaction, and the coordinator will need to call the microservices in the prepare and commit phases.

Saga - Saga pattern is asynchronous and reactive. In a Saga pattern, the distributed transaction is fulfilled by asynchronous local transactions on all related microservices. The microservices communicate with each other through an event bus. Saga pattern is its support for long-lived transactions. Because each microservice focuses only on its own local atomic transaction, other microservices are not blocked if a microservice is running for a long time. This also allows transactions to continue waiting for user input. Also, because all local transactions are happening in parallel, there is no lock on any object.
event messages could become difficult to maintain if the system gets complex. Another disadvantage of the Saga pattern is it does not have read isolation
</details>

### 3.  CAP therome
<details>
    <summary>
        Answer
    </summary> 
  Consistency: Every read receives the most recent write or an error
Availability: Every request receives a (non-error) response, without the guarantee that it contains the most recent write
Partition tolerance: The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes

When a network partition failure happens should we decide to
Cancel the operation and thus decrease the availability but ensure consistency
Proceed with the operation and thus provide availability but risk inconsistency
</details>

### 4.  creating indexes, even though they can improve the performance ?
<details>
    <summary>
        Answer
    </summary> 
  dadada.
</details>


### 5. optimistic and pessimistic locks should be used ?
<details>
    <summary>
        Answer
    </summary> 
  dadada.
</details>

### 6. short and long polling, compared to Web Sockets ?
<details>
    <summary>
        Answer
    </summary> 
  dadada.
</details>

### 7. NoSQL databases, when they can be useful, how they can help with optimization?
<details>
    <summary>
        Answer
    </summary> 
  dadada.
</details>
