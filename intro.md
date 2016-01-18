# Cassandra
Cassandra is massively linearly scalable NoSQL database

  - Fully distributed, with no single point of failure
  - Free and open source
  - Highly performant, with near-linear horizontal scaling in proper use cases

### Cassandra Query Language(CQL)
Cassandra models data using CQL.
CQL provides a familiar, row-column, SQL-like approach
  * CREATE, ALTER, DROP
  * SELECT, INSERT, UPDATE, DELETE

```SQL
CREATE TABLE Performer (
  name VARCHAR,
  country VARCHAR,
  style VARCHAR,
  born INT,
  died INT,
  PRIMARY KEY (name)
);
```

## Internal architecture

### Cluster
Cluster is a peer to peer (no master, no slaves) set of nodes.
  * **Node** - one Cassandra instance
  * **Rack** - a logical set of nodes with single point of failure
  * **Datacenter** - a logical set of racks.
  * **Cluster** – the full set of nodes which map to a single complete token ring
  
![alt text](/img/cassandra-cluster.jpg "Cassandra cluster")