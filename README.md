# turbopuffer (turbopuffer)

turbopuffer is a serverless search engine that combines vector and full-text (BM25) search built from first principles directly on object storage. It exposes a single REST API organized around namespaces — each namespace stores documents with vector embeddings, attributes, and full-text indexes — and supports approximate nearest neighbor, full-text BM25, and hybrid query patterns with attribute filtering, ranking, and aggregation. The platform is used in production by Anthropic, Cursor, Notion, Linear, Superhuman, Pylon, Readwise, and Telus, and handles 4T+ documents, 10M+ writes/s, and 25k+ queries/s across customer fleets. Official client libraries ship for Python, TypeScript, Go, Java, Ruby, and C#, generated from a public OpenAPI 3.1 specification via Stainless. Pricing is tiered (Launch, Scale, Enterprise) with usage-based metering on storage, writes, and queries on top of monthly minimums.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/turbopuffer/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/turbopuffer/refs/heads/main/apis.yml)

## Tags

- Vector Search
- Full-Text Search
- Hybrid Search
- BM25
- Serverless
- Object Storage
- RAG
- Semantic Search
- AI Infrastructure
- Embeddings

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-25

## APIs

### turbopuffer REST API

Single REST API for all turbopuffer operations — namespace metadata, write (upsert / patch / delete), vector ANN query, full-text BM25 query, hybrid query, multi-query, explain_query, branch_from, copy_from, and cache warming — with bearer-token authentication. The base host is region-templated as https://{region}.turbopuffer.com (e.g., gcp-us-east4.turbopuffer.com or aws-us-east-1.turbopuffer.com) to minimize egress and latency.

- **Human URL:** [https://turbopuffer.com/docs](https://turbopuffer.com/docs)
- **Base URL:** `https://api.turbopuffer.com`

#### Tags

- REST
- Vector Search
- Full-Text Search
- Hybrid Search

#### Properties

- [Documentation](https://turbopuffer.com/docs)
- [Authentication](https://turbopuffer.com/docs/auth)
- [Quickstart](https://turbopuffer.com/docs/quickstart)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/turbopuffer/main/openapi/turbopuffer-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Open A P I- Source](https://github.com/turbopuffer/turbopuffer-openapi)
- [Postman Collection](collections/turbopuffer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/turbopuffer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### turbopuffer Write API

Endpoints for upserting, patching, and deleting documents within a namespace. Writes are batched into a per-namespace write-ahead log and become queryable once committed to object storage. Supports both row-oriented and column-oriented batch formats.

- **Human URL:** [https://turbopuffer.com/docs/write](https://turbopuffer.com/docs/write)
- **Base URL:** `https://api.turbopuffer.com`

#### Tags

- Write
- Upsert
- Namespaces

#### Properties

- [Documentation](https://turbopuffer.com/docs/write)
- [Postman Collection](collections/turbopuffer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/turbopuffer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### turbopuffer Query API

Unified query endpoint that runs vector ANN, full-text BM25, and hybrid queries against a namespace, with attribute filters, top-k, aggregation groups, and ranking controls. Supports multi-query (up to 16 per request) and explain_query for query planning.

- **Human URL:** [https://turbopuffer.com/docs/query](https://turbopuffer.com/docs/query)
- **Base URL:** `https://api.turbopuffer.com`

#### Tags

- Query
- Vector
- BM25
- Hybrid
- ANN

#### Properties

- [Documentation](https://turbopuffer.com/docs/query)
- [Postman Collection](collections/turbopuffer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/turbopuffer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### turbopuffer Namespaces API

Namespace lifecycle and metadata endpoints — list namespaces, read schema / dimensions / row count, warm the cache, export contents, branch_from (copy-on-write clones in constant time), copy_from, and delete a namespace.

- **Human URL:** [https://turbopuffer.com/docs/namespaces](https://turbopuffer.com/docs/namespaces)
- **Base URL:** `https://api.turbopuffer.com`

#### Tags

- Namespaces
- Metadata
- Admin
- Branching

#### Properties

- [Documentation](https://turbopuffer.com/docs/namespaces)
- [Postman Collection](collections/turbopuffer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/turbopuffer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### turbopuffer Python SDK

Official Python client library for the turbopuffer REST API, Stainless-generated from the public OpenAPI spec.

- **Human URL:** [https://github.com/turbopuffer/turbopuffer-python](https://github.com/turbopuffer/turbopuffer-python)
- **Base URL:** `https://github.com/turbopuffer/turbopuffer-python`

#### Tags

- SDK
- Python

#### Properties

- [Repository](https://github.com/turbopuffer/turbopuffer-python)
- [Package](https://pypi.org/project/turbopuffer/)
- [Postman Collection](collections/turbopuffer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/turbopuffer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### turbopuffer TypeScript SDK

Official TypeScript / JavaScript client library for the turbopuffer REST API, Stainless-generated and published to npm.

- **Human URL:** [https://github.com/turbopuffer/turbopuffer-typescript](https://github.com/turbopuffer/turbopuffer-typescript)
- **Base URL:** `https://github.com/turbopuffer/turbopuffer-typescript`

#### Tags

- SDK
- TypeScript
- JavaScript

#### Properties

- [Repository](https://github.com/turbopuffer/turbopuffer-typescript)
- [Package](https://www.npmjs.com/package/@turbopuffer/turbopuffer)
- [Postman Collection](collections/turbopuffer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/turbopuffer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### turbopuffer Go SDK

Official Go client library for the turbopuffer REST API, Stainless-generated from the public OpenAPI spec.

- **Human URL:** [https://github.com/turbopuffer/turbopuffer-go](https://github.com/turbopuffer/turbopuffer-go)
- **Base URL:** `https://github.com/turbopuffer/turbopuffer-go`

#### Tags

- SDK
- Go

#### Properties

- [Repository](https://github.com/turbopuffer/turbopuffer-go)
- [Postman Collection](collections/turbopuffer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/turbopuffer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### turbopuffer Java SDK

Official Java / Kotlin client library for the turbopuffer REST API, Stainless-generated from the public OpenAPI spec.

- **Human URL:** [https://github.com/turbopuffer/turbopuffer-java](https://github.com/turbopuffer/turbopuffer-java)
- **Base URL:** `https://github.com/turbopuffer/turbopuffer-java`

#### Tags

- SDK
- Java
- Kotlin

#### Properties

- [Repository](https://github.com/turbopuffer/turbopuffer-java)
- [Postman Collection](collections/turbopuffer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/turbopuffer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### turbopuffer Ruby SDK

Official Ruby client library for the turbopuffer REST API, Stainless-generated from the public OpenAPI spec.

- **Human URL:** [https://github.com/turbopuffer/turbopuffer-ruby](https://github.com/turbopuffer/turbopuffer-ruby)
- **Base URL:** `https://github.com/turbopuffer/turbopuffer-ruby`

#### Tags

- SDK
- Ruby

#### Properties

- [Repository](https://github.com/turbopuffer/turbopuffer-ruby)
- [Postman Collection](collections/turbopuffer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/turbopuffer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### turbopuffer C# SDK

Official C# / .NET client library for the turbopuffer REST API, Stainless-generated from the public OpenAPI spec.

- **Human URL:** [https://github.com/turbopuffer/turbopuffer-csharp](https://github.com/turbopuffer/turbopuffer-csharp)
- **Base URL:** `https://github.com/turbopuffer/turbopuffer-csharp`

#### Tags

- SDK
- CSharp
- DotNet

#### Properties

- [Repository](https://github.com/turbopuffer/turbopuffer-csharp)
- [Postman Collection](collections/turbopuffer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/turbopuffer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### tpuf-benchmark

Open-source general-purpose benchmarking tool for turbopuffer deployments. Useful for validating recall, latency, and throughput on a given workload.

- **Human URL:** [https://github.com/turbopuffer/tpuf-benchmark](https://github.com/turbopuffer/tpuf-benchmark)
- **Base URL:** `https://github.com/turbopuffer/tpuf-benchmark`

#### Tags

- Tooling
- Benchmark
- Go

#### Properties

- [Repository](https://github.com/turbopuffer/tpuf-benchmark)
- [Postman Collection](collections/turbopuffer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/turbopuffer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://turbopuffer.com/)
- [Documentation](https://turbopuffer.com/docs)
- [Git Hub](https://github.com/turbopuffer)
- [OpenAPI](https://github.com/turbopuffer/turbopuffer-openapi) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Pricing](https://turbopuffer.com/pricing)
- [Architecture](https://turbopuffer.com/docs/architecture)
- [Regions](https://turbopuffer.com/docs/regions)
- [Limits](https://turbopuffer.com/docs/limits)
- [Blog](https://turbopuffer.com/blog)
- [L L Ms Txt](https://turbopuffer.com/llms.txt)
- [Terms of Service](https://turbopuffer.com/terms-of-service)
- [Customers](https://turbopuffer.com/customers)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
