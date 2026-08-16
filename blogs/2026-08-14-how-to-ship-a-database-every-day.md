---
title: "How to ship a database every day"
url: "https://turbopuffer.com/blog/control-plane"
date: "2026-08-14"
feed_url: "https://turbopuffer.com/blog/rss.xml"
---
We deploy many database upgrades every day across ~100 public, single-tenant, and BYOC clusters. It would be insane to use Terraform or Helm to do that, so we built our own control plane.
