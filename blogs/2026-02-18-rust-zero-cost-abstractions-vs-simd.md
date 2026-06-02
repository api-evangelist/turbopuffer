---
title: Rust zero-cost abstractions vs. SIMD
url: https://turbopuffer.com/blog/zero-cost
date: '2026-02-18'
author: ''
feed_url: https://turbopuffer.com/blog/rss.xml
---
A customer query was taking over 4× longer than it should have. The profiler pointed at Rust code we'd assumed was free. We followed the trail all the way down to assembly to find the true cost.
