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
   
Optimistic Locking is a strategy where you read a record, take note of a version number (other methods to do this involve dates, timestamps or checksums/hashes) and check that the version hasn't changed before you write the record back. When you write the record back you filter the update on the version to make sure it's atomic. (i.e. hasn't been updated between when you check the version and write the record to the disk) and update the version in one hit.

If the record is dirty (i.e. different version to yours) you abort the transaction and the user can re-start it.

This strategy is most applicable to high-volume systems and three-tier architectures where you do not necessarily maintain a connection to the database for your session. In this situation the client cannot actually maintain database locks as the connections are taken from a pool and you may not be using the same connection from one access to the next.

Pessimistic Locking is when you lock the record for your exclusive use until you have finished with it. It has much better integrity than optimistic locking but requires you to be careful with your application design to avoid Deadlocks. To use pessimistic locking you need either a direct connection to the database (as would typically be the case in a two tier client server application) or an externally available transaction ID that can be used independently of the connection.
</details>

### 6. short and long polling, compared to Web Sockets ?
<details>
    <summary>
        Answer
    </summary> 
    Short polling.
Send a request to the server, get an instant answer. Do this every x seconds, minutes etc. to keep your application up-to-date. But: This costs a lot of requests.
    Long polling
Send a request to the server, keep the connection open, get an answer when there's "data" for you. This will cost you only one request (per user), but the request keeps a permanent connection between client and server up
  Long polling- potentially when you are exchanging single call with server, and server is doing some work in background. Also when you won't query server on the same page anymore. Also when you are not using php as layer to handle the long polled connection (node/c++ can be a simple middle layer). Note long polling can be really beneficial, but only when you make it so.
Websocket- you potentially will exchange more then one or two calls with server, or something might come from server you did not expected / asked, like notification of email or something. You should plan different "rooms", depend on functionalities. Embrace the event based nature of javascript
</details>

### 7. NoSQL databases, when they can be useful, how they can help with optimization?
<details>
    <summary>
        Answer
    </summary> 
  dadada.
</details>
