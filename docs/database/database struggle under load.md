# Database Load Struggles

The phrase "Database struggling under high read & write loads" means:

> The database is experiencing performance issues because it's receiving too many requests to read (fetch data) and write (insert/update/delete data) at the same time.

### Breaking it down:
* <b>Read load</b>: When users or systems are frequently retrieving data from the database.
* <b>Write load</b>: When data is being added, updated, or deleted very often.

### When a database `struggles`:
It may lead to:
* Slow queries: Data retrieval or updates take longer.
* Timeouts: Operations may fail if they take too long.
* Crashes: In extreme cases, the database can become unresponsive.
* Lock contention: Multiple operations trying to access or modify the same data can block each other.

### Causes:
* Too many users at once (high traffic).
* Poorly optimized queries or indexes.
* Insufficient hardware resources (CPU, RAM, IOPS).
* Database engine limitations.

### Example 
Imagine an online store during a flash sale. Thousands of users are:
* Viewing product pages (read load).
* Placing orders (write load).

> If the database isn't scaled or optimized properly, it might not keep up, causing delays or failures.
