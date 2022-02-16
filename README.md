# MariaDB Replication on Docker

## Introduction

In this workshop, I'll demonstrate how to configure a simple HA MariaDB replication. We will configure three MariaDB servers, `master1`, `master2` and `slave1`.  
The servers are running `MariaDB 10.6.5`. We have one active master `master1`, one passive master `master2`, and a slave, `slave1`, replicating from the active master `master1`. The active and passive masters are set up to replicate Master-Master.

- Master-to-Master replication: `master1` <----> `master2`
. In a Master-to-Master replication `master2` will be the slave of `master1` and `master1` will be the slave of `master2`. 
- Master-to-Slave replication: 	`master1` ----> `slave1`
		
        +---------+                  +---------+
        | Master1 | <--------------> | Master2 |
        +---------+                  +---------+
            \
             \
              \
               \
                V
           +----------+
           |  Slave1  |
           +----------+

## Requirements:

* Familiarity with basic [MySQL](https://www.mysqltutorial.org/) commands.
* Familiarity with [Docker](https://www.docker.com/).
* Docker Desktop installed locally.

## Short version
This is the [short version](MariaDB-Replication-Short.md) . Just follow the steps in order.

## Long version
This is the [long version](MariaDB-Replication-Long.md) .
