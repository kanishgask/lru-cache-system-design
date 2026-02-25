# 🏗️ Architecture - LRU Cache System

Client
   ↓
Application Layer
   ↓
LRU Cache Layer
   ↓
Database (Optional Fallback)

---

Flow:

1. Client sends request
2. Check LRU Cache
   - If hit → return immediately
   - If miss → fetch from DB → store in cache → return

---

Benefits:

- Reduces DB load
- Improves response time
- Handles frequent access efficiently
