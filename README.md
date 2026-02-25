# 🗂️ LRU Cache - System Design + Low Level Design

> Day 3 – High-Package Software Engineer Journey 🚀

---

## 📌 Problem Statement

Design and implement an LRU (Least Recently Used) Cache with:

- O(1) time complexity for get()
- O(1) time complexity for put()
- Fixed capacity
- Automatic eviction of least recently used item

---

# 🧠 Why LRU Cache?

Used in:
- Database caching
- Redis
- CPU memory management
- Web caching
- CDN systems

---

# 🎯 Functional Requirements

- get(key) → Return value if exists
- put(key, value) → Insert/update key
- Remove least recently used item when capacity exceeded

---

# ⚙️ Non-Functional Requirements

- Fast operations
- Memory efficient
- Thread-safe (future improvement)

---

# 🏗️ Design Approach

To achieve O(1):

Data Structures Used:

1️⃣ HashMap (Dictionary)
- Fast lookup by key

2️⃣ Doubly Linked List
- Maintain usage order
- Move accessed nodes to head
- Remove from tail when capacity full

---

# 📊 Why Not Use Only Array or List?

Array → O(n) removal  
List → O(n) search  

Combination of HashMap + Doubly Linked List = O(1)

---

# 🔄 Operations Flow

## get(key)

- If key exists:
  - Move node to front (most recently used)
  - Return value
- Else:
  - Return -1

## put(key, value)

- If key exists:
  - Update value
  - Move to front
- Else:
  - If capacity reached:
      Remove tail node
  - Insert new node at head

---

# 📈 Time & Space Complexity

| Operation | Time Complexity |
|-----------|-----------------|
| get()     | O(1) |
| put()     | O(1) |

Space Complexity: O(capacity)

---

# ⚡ Scaling Considerations

- Can be sharded across multiple nodes
- Useful as local in-memory cache in microservices
- Can integrate with Redis for distributed caching

---

# 🚀 Future Improvements

- Thread safety using locks
- TTL (Time To Live)
- LFU implementation comparison
- Metrics monitoring

---

# 🎯 Concepts Demonstrated

- Low-Level Design
- Data Structures
- Memory Optimization
- Cache Eviction Policies
- Backend System Thinking

---

⭐ Part of 30-Day Elite Engineering Series
