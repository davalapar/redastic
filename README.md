# redastic
An experimental document management.

* uses ajv for schema creation and validation
* uses what-the-pack for binary serialization
* uses redis for storage and transactions
* uses elasticsearch for indexing and providing search capabilities

## components

* Schema
* Entity
  * has kind
  * has id
  * has data
  * uses schemas
  * supports upsert(data), merge(data)
* Transactions
  * allows multiple entities
  * validates schemas
  * gracefully handles errors
* Query
  * has sorts, filters, limit
  * has cursors / pagination support
  * supports first(), transform(fn)
