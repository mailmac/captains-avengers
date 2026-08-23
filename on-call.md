---
layout: page
title: On-call resolution guide
description: Move from alert → symptoms → diagnosis → resolution → escalation.
permalink: /on-call/
---

## 01 · The alert

> **Example: Database connection pool exhausted**

Triggered when the production API returns HTTP 5xx responses above the configured threshold for five consecutive minutes.

## 02 · The product

**Product:** Captain's Avengers API

Customer-facing service responsible for serving application requests and coordinating downstream integrations.

## 03 · Steps to diagnose

1. **Confirm scope.** Check whether errors affect all requests or a single endpoint.
2. **Check recent changes.** Review the latest deployment, configuration changes, and feature flags.
3. **Inspect dependencies.** Check database, queues, third-party APIs, and other downstream services.
4. **Review telemetry.** Compare error rate, latency, request volume, and resource saturation.
5. **Mitigate first.** If customer impact is active, use the approved rollback, feature-flag, or traffic-management procedure.

## 04 · Symptoms of the alert

- HTTP 5xx responses increase above the alert threshold.
- API latency may increase before error rates spike.
- Customer requests may fail or time out.
- Downstream dependency failures may appear in application logs.

## 05 · Escalation path

| Priority | Owner              | When to escalate                                           |
| -------- | ------------------ | ---------------------------------------------------------- |
| 1        | Primary on-call    | Own initial diagnosis and mitigation.                      |
| 2        | Service owner      | Application-level expertise is required.                   |
| 3        | Platform / SRE     | Infrastructure, networking, capacity, or platform failure. |
| 4        | Incident commander | Sustained or high-severity customer impact.                |
