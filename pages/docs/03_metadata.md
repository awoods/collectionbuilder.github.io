---
layout: docs-default
title: Metadata
permalink: /docs/metadata.html
section: metadata
step: 3
---

{% assign parts = site.docs | where: 'section','metadata' | sort: 'section_order' %}

{{ parts }}