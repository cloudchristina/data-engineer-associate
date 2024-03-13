## Foudamentals

#### data type
1. structured data
2. unstructured data
3. semi-structured data

#### Property: 3Vs
1. volume: amount, size of data, ?process, ?storing, ?analyzing
2. velocity: new data is generated, collected, processed, 
   - IoT - less streaming data, 
   - trading
3. variety: type, structure, sources of data, 
   - emails, json logs, healthcare records

### Data warehouse
- data repo, for ready-heavy operations
- Redshift
- Google BigQuery
- Azure SQL data warehouse
- Schema-on-write: predefined schema before writing data
- transformed data: ETL 
- mainly structured data, less agile, more expensive
- BI & analytics are primary use case

clickstream data, purchase data, catalog data -> data warehouse -> accounting data mart, analysis data mart, machine learning data mart


### Data lake
- storage repo
- raw data, can be queried
- s3, azure data lake storage, Hadoops distributed file system
- s3-> Glue-> Athena
- Schema on read, ELT or just load for storage purpose
- both unstructured or structured, cost effective
- advanced analytics, ML, data discovery are key goals

### Data lakehouse
- hybrid
- combine both data warehouse and data lake
- allow schema on write and read
- delta lake, bring acid transactions to big data
- **lake formation**: s3 and redshift spectrum
- databricks lakehouse platform
- azure synapse analytics

#### Data mesh
- self-service with own domain

### ETL pipeline
1. E
- move data from source into data warehouse
- can be done in real-time or in batches
- ensure data integrity

2. transform various operations:
- data cleansing: removing duplicates, fix errors
- data enrichment: adding additional data
- format changes: date, string manipulation
- aggregations or computations: totals or averages
- encoding or decoding
- handle missing values

3. Load
- batches
- streaming

4. automate 
- ETL pipeline
- Glue
- event bridge
- step function
- apache airflow
- glue

#### Data sources
1. JDBC
- java db connectivity
- platform independent
- language-dependent

2. ODBC
- object db connectivity
- platform dependent
- language independent

3. Raw logs
4. API's
5. Streams
- kafka

### CSV
- human readable
- comma-separated values
- text-based format
- small to medium
- editable data storage
- importing exporting data from db or spreadsheets
- Systems: SQL-based, excel, pandas in python, R

### JSON
- js object notation
- text-based, human-readable
- key value pairs
- web servers, web client
- config, settings
- flexible schema or nested data structures: more layers
- systems: web browsers, js, python, java, restful apis, Nosql

### Avro
- binary format
- both data and schema
- big data, real time processing
- schema evolution
- efficient serialization for data transport between systems
- Apache kafka, spark, flink, hadoop

### Parquet
- columnar storage format
- analytics
- for compressions and encoding
- systems: hadoop, Kafka spark, hive, impala, redshift spectrum

### Data lineage
- tracking record
- compliance
- understanding how transformed

### schema evolution
- glue schema registry

### Data skew mechanism
- unequal distribution or imbalance across nodes

address:
- adaptive partitioning
- salting
- repartitioning
- sampling
- custom partitioning

### Data validation & profiling
1. completeness
   - no missing
2. Consistency
   - cross-field validation
3. Accuracy
   - compare with trusted sources
4. integrity

### SQL
- Aggregation
  - Count
  - Sum
  - AVG
  - Max/Min
  - CASE: 
   - different way from Where clauses
  - Grouping
  - Nesting grouping, sorting 
  - Pivoting: row-> column

### SQL join type
- Inner Join
- left outer join
- right outer join
- full outer join
- cross outer join

### SQL regular expressions
- pattern matching
~ regular expression operator
~*: case-insenstive
!~*: not match, case insenstive
| : alternate characters
[a-z]: lowercase
[a-z]{4}: match any 4-letter lower case
^: start of string - carrot
\d: any digit
\w: any letter, digit or _
\s: whitespace
\t: tab


