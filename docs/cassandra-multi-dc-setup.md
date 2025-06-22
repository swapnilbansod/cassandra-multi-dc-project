# Cassandra Multi-DC Setup Guide

## Data Centers

- DC1: India Region (e.g., ap-south-1)
- DC2: Europe Region (e.g., eu-central-1)

## Steps Performed

1. VPC Peering setup between regions
2. Cassandra installed on EC2 in each region
3. Configured `cassandra.yaml` with seed nodes across both DCs
4. Set snitch to `GossipingPropertyFileSnitch`
5. Used `NetworkTopologyStrategy` for keyspace

```sql
CREATE KEYSPACE <your_keyspace> WITH REPLICATION = {
  'class': 'NetworkTopologyStrategy',
  'DC1': 3,
  'DC2': 3
};

Validated node status with:
nodetool status
nodetool gossipinfo



