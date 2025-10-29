Follow the steps below to set up Neo4j Desktop, create a project and database, and import your CSV files for querying:

1. Download and Install Neo4j Desktop
   • Visit the official Neo4j website: https://neo4j.com/download/
   • Download and install Neo4j Desktop suitable for your operating system.
2. Create a New Project and Database
   • Open Neo4j Desktop and click on "New Project" to create a new project.
   • Inside the project, click "Add Graph" → "Create a Local Graph".
   • Set the Database Name, Username, and Password.
   • Click "Create" and then "Start" to run your database.
3. Add CSV Files to the Import Folder
   • Locate the import folder for your database:
   o Right-click on the database in Neo4j Desktop and select "Open Folder" → "Import".
   • Paste your required .csv files into this folder. This makes them accessible for LOAD CSV queries in the Neo4j Browser.
4. Open Neo4j Browser and Load the Data
   • Click "Open in Browser" for your running database.
   • Use Cypher (CQL) queries to load data

Neo4j is a graph database management system based on the property graph model. Unlike relational databases that use tables, Neo4j stores data as nodes, relationships, and properties, which makes it ideal for representing and querying connected data.
• Nodes
• Represent entities (e.g., a person, product, location).
• Can have labels (e.g., Person, Movie) to define their type.
• Can hold properties (key-value pairs).
• Relationships
• Represent connections between nodes.
• Are directed (e.g., ACTED_IN, FRIEND_OF).
• Can also have properties.
• Properties
• Attributes of nodes or relationships.
• Stored as key-value pairs (e.g., name: "Alice").
• Labels and Types
• Labels classify nodes.
• Relationship types define the nature of the relationship.
• Cypher Query Language (CQL)
• Neo4j uses Cypher, a declarative query language similar to SQL but optimized for graphs.
• Example:
cypher
CopyEdit
MATCH (a:Person)-[:FRIEND_OF]->(b:Person)  
RETURN a.name, b.name
