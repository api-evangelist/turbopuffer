---
title: Why BM25 queries with more terms can be faster (and other scaling surprises)
url: https://turbopuffer.com/blog/bm25-latency-musings
date: '2026-01-07'
author: ''
feed_url: https://turbopuffer.com/blog/rss.xml
---
I analyzed how BM25 query latencies scale with document count and top_k. Longer queries scale less efficiently, and essential terms impact performance in some surprising ways.
