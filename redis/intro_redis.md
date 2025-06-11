# Intro to Redis

Redis (Remote Dictionary Server) is an open-source, in-memory data structure store used as a database, cache, and message broker.

---

## 🚀 What is Redis?

* High-performance key-value store
* In-memory storage with optional persistence
* Supports rich data types: strings, hashes, lists, sets, sorted sets, bitmaps, hyperloglogs, and streams

---

## 🎯 Use Cases

* **Caching**: Store frequently accessed data
* **Session Store**: Save user session data
* **Real-time Analytics**: Leaderboards, counters
* **Message Queue**: Pub/Sub architecture

---

## ⚙️ Basic Commands

```bash
# Set a key
SET mykey "Hello Redis"

# Get a key
GET mykey

# Delete a key
DEL mykey

# Increment a value
INCR counter

# List all keys
KEYS *
```

---

## 🏗️ Redis with Docker

```bash
# Run Redis container
docker run --name redis-server -d -p 6379:6379 redis

# Access Redis CLI
docker exec -it redis-server redis-cli
```

---

## ✅ Tip

Redis is single-threaded and extremely fast—ideal for microservices and distributed apps.
