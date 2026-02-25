# 📊 ER Diagram - LRU Cache

Even though this is an in-memory system, conceptually we have:

CACHE
- key (Primary Key)
- value
- usage_order
- capacity

Relationship:
Cache holds multiple nodes ordered by recency.

---

ASCII Representation:

HEAD <-> Node1 <-> Node2 <-> Node3 <-> TAIL

HashMap:
key → Node Reference
