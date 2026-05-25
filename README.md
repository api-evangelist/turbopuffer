# turbopuffer

API Evangelist profile of **turbopuffer** — a serverless search engine that
combines vector and full-text (BM25) search built directly on object storage.

- Website: https://turbopuffer.com/
- Docs: https://turbopuffer.com/docs
- Pricing: https://turbopuffer.com/pricing
- GitHub: https://github.com/turbopuffer
- Public OpenAPI: https://github.com/turbopuffer/turbopuffer-openapi
- LLMs.txt: https://turbopuffer.com/llms.txt

## What's in this repo

| Path | Contents |
|---|---|
| `apis.yml` | APIs.json 0.19 profile — APIs, SDKs, common properties, integrations |
| `openapi/turbopuffer-openapi.yml` | Official OpenAPI 3.1 spec mirrored from `turbopuffer/turbopuffer-openapi` |
| `plans/turbopuffer-plans-pricing.yml` | API Commons Plans 0.1 — Launch / Scale / Enterprise tiers |
| `rate-limits/turbopuffer-rate-limits.yml` | API Commons Rate Limits 0.1 — published per-namespace caps and quotas |
| `finops/turbopuffer-finops.yml` | FinOps Framework / FOCUS 1.3 alignment |

## API surface

- Single REST API rooted at `https://{region}.turbopuffer.com`
- Bearer-token authentication
- Namespace-oriented data model with branching (copy-on-write), pinning,
  schema introspection, multi-query, and explain_query
- Vector ANN, full-text BM25, and hybrid query patterns with attribute
  filters, top-k, ranking, and aggregation

## Notable customers and integrations

Anthropic, Cursor, Notion, Linear, Superhuman, Pylon, Readwise, and Telus
run on turbopuffer in production. Cursor alone reports 1T+ vectors and 80M+
namespaces, with up to 23.5% improvement in AI agent accuracy versus
grep-only retrieval and a 20x cost reduction over prior infrastructure.

Official client libraries — Python, TypeScript, Go, Java, Ruby, and C# — are
Stainless-generated from the public OpenAPI 3.1 specification.
