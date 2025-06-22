# cassandra-multi-dc-project
# Cassandra Multi-Datacenter Deployment (v4.0)

Real-world implementation of a Cassandra 4.0 multi-datacenter setup across two cloud regions using AWS EC2 instances.

## Project Overview
- **Type**: Database Infrastructure
- **Tech**: Cassandra 4.0.x, Linux, EC2, VPC Peering
- **Tools**: nodetool, bash, Prometheus, Grafana
- **Purpose**: HA and cross-region DR

##  Project Contents

| Folder | Description |
|--------|-------------|
| `docs/` | Setup documentation and architecture |
| `config/` | Cassandra configuration samples |
| `scripts/` | Operational scripts |
| `SOP/` | Maintenance and DR procedures |

##  Key Highlights
- Setup of 2 data centers in different cloud regions
- Configured `NetworkTopologyStrategy`
- Automated status check and restart SOPs

##  Architecture

![Multi-DC Architecture](docs/architecture-diagram.png)
