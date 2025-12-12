# SPL Queries for DNS Lab

## Task 1: Most frequently queried domains
index=dns_lab sourcetype="json"
| stats count by query
| sort -count

## Task 2: Most active user IPs
index=dns_lab sourcetype="json"
| stats count by id.orig_h
| sort -count

## Task 3: Breakdown of DNS query types
index=dns_lab sourcetype="json"
| stats count by qtype
