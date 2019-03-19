# Avro Tools

download - https://mvnrepository.com/artifact/org.apache.avro/avro-tools/1.8.2

**<u>use to print avro files in readable format :</u>** 

- java -jar avro-tools.jar tojson --pretty customer-generic.avro
- java -jar avro-tools-1.8.2.jar getschema customer-generic. Avro



### Schema evolution 

There are 3 types of schema evolutions

- Backward compatible: *use new schema to read old data*
  - **example** : adding new field with default value
- Forward compatible : *use old schema to read new data*
  - **example** : *adding new field with default value*
  - **Full compatible :**  
    - *Only add fields with defaults*
    - *only remove fields with defaults*



### Schema Registry

------

- *Store and retrieve schemas for producers / consumers*
- *Enforce Backward/forward / fully compatible on topics*
- *Decrease the size of the payload of data sent to Kafka*

#### Operations

- *Add schema*
- *retrieve schema*
- *update schema*
- *delete a schema*
- *all through using REST API*
- *Schemas can be applied to Key and values*



### Avro console producer and consumer

```shell
# console producer
kafka-avro-console-producer \
--broker-list 192.168.99.100:9092 \
--topic test-avro \
--property schema.registry.url=http://127.0.0.1:8081 \
--property value.schema='
{"type":"record","name":"myrecord",
"fields":[{"name":"f1","type":"string"}]    
}'
```



















