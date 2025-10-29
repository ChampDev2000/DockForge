### Install docker desktop
### check docker version using 
`docker version`  \
`docker-compose up -d `

### for running node1 - 
docker exec -it 2025GRP01-node1 cqlsh 

### create keyspace 
create keyspace demo with replication = {"class" : "SimpleStrategy", "replication_factor" : 2};

use demo;
### create table - 
create table demoTable(id int primary key, name varchar(90)); 

### insert data - 
insert into demoTable(id , name ) values (1, "Ram"); 

### for running node2 - 
docker exec -it 2025GRP01-node2 cqlsh \
select * from demoTable;
