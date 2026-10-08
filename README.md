# Awesome-In-Memory-Caching-Redis-Memcached

## Top In-Memory Caching (Redis/Memcached) Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Managed Cache Services, Redis/Memcached Alternatives & Self-Hosted Caching*  

**Last updated: October 2026**



This repository tracks notable **commercial managed caching platforms** and **open-source projects** that provide in-memory caching and key-value storage — from fully managed cloud services to community-driven Redis forks and high-performance alternatives.



**Examples** include Amazon ElastiCache, Redis Enterprise Cloud, Upstash Redis, Memurai, Azure Cache for Redis, Google Cloud Memorystore, Aiven for Redis, Momento Serverless Cache, Dragonfly Cloud, and Hazelcast Cloud (the category leaders).



**Open-source emphasis**: The Redis ecosystem underwent a major licensing shift in 2024–2025, with **Valkey** emerging as the Linux Foundation BSD-3-Clause successor backed by AWS, Google, and Oracle . **Dragonfly** delivers multi-threaded performance with 2.5–3.5x Redis throughput under high concurrency . **KeyDB** brings active-active replication . **Garnet** from Microsoft Research provides .NET-native Redis compatibility . **Memcached** remains the lightweight caching standard. **DiceDB** adds cache spill-to-disk, while **SugarDB** and **BuntDB** serve embedded use cases. This section is heavily expanded.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Amazon ElastiCache](https://aws.amazon.com/elasticache/)**  

  **AWS's fully managed caching service** — supports Redis, Memcached, and **Valkey** . **Serverless option** for automatic scaling . **As of 2025, AWS defaults new clusters to Valkey unless explicitly overridden** . **Best for AWS-native caching workloads** .



- **[Redis Enterprise Cloud](https://redis.com/cloud/)**  

  **The commercial Redis platform** — fully managed with active-active geo-distribution and modules . **Pricing scales with throughput and memory** . **Best for enterprises wanting Redis with commercial support** .



- **[Upstash Redis](https://upstash.com/redis)**  

  **Serverless Redis** — pay-per-request pricing with global replication . **REST API and low latency** . **Best for serverless applications** .



- **[Memurai](https://www.memurai.com/)**  

  **Redis-compatible cache for Windows** — native Windows service with Redis compatibility . **Best for Windows-centric environments** .



- **[Azure Cache for Redis](https://azure.microsoft.com/en-us/products/cache/)**  

  **Microsoft's managed Redis** — integrated with Azure ecosystem . **Note**: Enterprise tiers retire 31 March 2027; Basic/Standard/Premium retire 30 September 2028. Migration to **Azure Managed Redis** is the destination .



- **[Google Cloud Memorystore](https://cloud.google.com/memorystore)**  

  **Google's managed caching** — supports Redis, Memcached, and **Valkey** as fully managed options . **Best for GCP-native caching** .



- **[Aiven for Redis](https://aiven.io/redis)**  

  **Managed Redis on multiple clouds** — available on AWS, GCP, Azure, and DigitalOcean . **Best for multi-cloud Redis** .



- **[Momento Serverless Cache](https://www.gomomento.com/)**  

  **Serverless caching platform** — pay-per-use with sub-millisecond latency . **Best for serverless architectures** .



- **[Dragonfly Cloud](https://www.dragonflydb.io/)**  

  **Managed Dragonfly** — multi-threaded architecture for 25x throughput over single-threaded engines . **Best for high-performance caching** .



- **[Hazelcast Cloud](https://hazelcast.com/)**  

  **In-memory data grid** — distributed caching and computing . **Best for distributed caching at scale** .



## Open-Source GitHub Projects



### Redis-Compatible Caches



- **[Valkey](https://github.com/valkey-io/valkey)**  

  **The primary community-driven open-source successor to Redis**, BSD-3-Clause licensed . **Linux Foundation project backed by AWS, Google, and Oracle** . **Fully free with no license restrictions** . **Retains Redis core data structures, persistence, replication, Sentinel, clustering, Lua scripting, and transactions** — existing Redis clients can connect directly . **Valkey 8.0 introduced enhanced I/O multithreading** with reports of up to 1.19 million requests per second . **Provides BSD-licensed equivalents to Redis Stack modules**: valkey-json, valkey-bloom, valkey-search, valkey-ldap . **Best for organizations requiring permissive licensing and community governance** .



- **[Redis 8](https://github.com/redis/redis)**  

  **Redis under AGPLv3 licensing** (additional option alongside RSALv2/SSPLv1), with Redis Stack modules integrated into core . **Significant performance improvements**: up to 87% faster commands and 2x throughput over earlier releases . **Includes JSON, Time Series, probabilistic data types, and Query Engine** . **Best for teams needing Redis Stack modules under open-source licensing** .



- **[Dragonfly](https://github.com/dragonflydb/dragonfly)**  

  **Modern ultra-fast in-memory data store**, BSL 1.1 licensed with additional use grant . **Multi-threaded, shared-nothing architecture** — partitions keyspace between threads for vertical scaling . **Consistently delivered 2.5–3.5x ops/sec of original Redis under high concurrency** . **Memory efficiency: same data used 15–22% less RAM** . **Supports Redis and Memcached APIs, snapshots, replication, expiry, and eviction** . **Best for memory or CPU-constrained workloads** .



- **[KeyDB](https://github.com/Snapchat/KeyDB)**  

  **Multi-threaded Redis fork from Snapchat**, BSD-3-Clause licensed . **Multithreaded networking and query processing** leveraging multiple CPU cores . **Active-active replication** — multiple instances can accept writes and replicate to each other . **FLASH storage for large datasets and subkey expiration** . **Trade-off**: Slower development cadence than Valkey, Redis, or Dragonfly . **Best for active-active replication requirements** .



- **[Garnet](https://github.com/microsoft/garnet)**  

  **Microsoft Research's Redis-compatible implementation**, MIT licensed . **Built on modern .NET runtime with native multithreading and lock-free data structures** . **Async-optimized network I/O and minimal garbage collection overhead** . **Trade-off**: Only ~70% Redis API compatibility . **Best for .NET-centric environments** .



- **[DiceDB](https://github.com/DiceDB/dice)**  

  **In-memory real-time database with SQL-based reactivity**, fork of Valkey . **Drop-in replacement for Redis** — fully compatible with Valkey and Redis tooling . **dicedb-spill module**: transparently persists evicted keys to disk using RocksDB and restores them on cache misses . **Best for real-time applications needing cache spill to disk** .



### Memcached & Alternatives



- **[Memcached](https://github.com/memcached/memcached)**  

  **The classic distributed memory object caching system**, BSD-3-Clause licensed with **13,000+ GitHub stars** . **Simple, fast key-value caching** . **The standard for simple caching** . **Best for straightforward caching needs** .



- **[Memcached (Windows port)](https://github.com/memcached/memcached)** — Community Windows builds available .



- **[twemproxy](https://github.com/twitter/twemproxy)**  

  **Twitter's fast proxy for Memcached and Redis**, Apache-2.0 licensed . **Connection pooling and sharding** . **Best for scaling Memcached/Redis** .



- **[Mcrouter](https://github.com/facebook/mcrouter)**  

  **Facebook's Memcached protocol router**, MIT licensed . **Scales Memcached deployments** with consistent hashing and failover . **Best for large-scale Memcached** .



### Embedded & Alternative Caches



- **[SugarDB](https://github.com/EchoVault/SugarDB)**  

  **Embeddable and distributed in-memory alternative to Redis**, Apache-2.0 licensed with **498 GitHub stars** . **Go-based with LFU/LRU caching, pub/sub, and cluster support** . **Best for embedded Go applications** .



- **[BuntDB](https://github.com/tidwall/buntdb)**  

  **Embeddable in-memory key/value database for Go**, MIT licensed . **Supports spatial indexes and custom indexes** . **Best for embedded Go applications** .



- **[Ristretto](https://github.com/dgraph-io/ristretto)**  

  **In-memory cache library for Go**, Apache-2.0 licensed . **High performance with LRU, LFU, ARC eviction** . **Best for Go caching** .



- **[Caffeine](https://github.com/ben-manes/caffeine)**  

  **High-performance in-memory caching library for Java**, Apache-2.0 licensed . **Near-optimal hit rate with Window TinyLFU** . **Best for Java applications** .



- **[Apache Ignite](https://github.com/apache/ignite)**  

  **Distributed in-memory computing platform**, Apache-2.0 licensed . **Persistence, SQL, and compute grid** . **Best for distributed caching and computing** .



- **[Hazelcast](https://github.com/hazelcast/hazelcast)**  

  **Unified real-time data platform**, Apache-2.0 licensed . **Stream processing with fast data store** . **Best for distributed caching at scale** .



### Additional Strong Open-Source Options



- **tinyredis** — Redis-compatible server in Go with Raft clustering .

- **Redka** — Redis re-implemented with SQLite .

- **Skytable** — NoSQL database with Redis-like API .

- **EchoVault** — Distributed in-memory data store (successor to SugarDB) .

- **NCache** — .NET distributed cache (commercial with open-source core) .



**Frameworks for building custom in-memory caching solutions**: Combine **Valkey** for the safest permissively-licensed Redis replacement with full command compatibility . Use **Dragonfly** when vertical scaling and multi-core utilization are the primary goals . Deploy **KeyDB** for active-active replication requirements . Choose **Redis 8** when Redis Stack modules are essential and AGPLv3 is acceptable . Integrate **Garnet** for .NET-centric environments with partial Redis API needs . Use **DiceDB** for cache spill-to-disk capabilities . Choose **Memcached** for simple, straightforward caching . Use **Caffeine** for Java applications and **Ristretto** for Go applications . Note that managed caching with global infrastructure, automatic scaling, and vendor-supported SLAs (Amazon ElastiCache, Redis Enterprise Cloud, Azure Cache for Redis) remains primarily commercial territory; open-source stacks provide strong in-memory storage, caching, and persistence foundations that require integration for complete managed deployments.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- In-memory caching platforms handle sensitive application data. Self-hosted solutions require proper security hardening, access controls, encryption at rest and in transit, and compliance with data privacy regulations.

- **License considerations**: Valkey uses BSD-3-Clause , Redis 8 uses AGPLv3/RSALv2/SSPLv1 , Dragonfly uses BSL 1.1 , KeyDB uses BSD-3-Clause , and Garnet uses MIT . Verify licensing against your use case before committing.

- **Redis API compatibility varies**: Valkey ~100% , KeyDB ~95% , Garnet ~70% . Module dependencies (Redis Stack, custom modules) are the most common migration blocker — check before committing to a fork .

- **Azure Cache for Redis retirement**: Enterprise tiers retire 31 March 2027; Basic/Standard/Premium retire 30 September 2028. Migration to Azure Managed Redis is the destination .

- The open-source ecosystem provides strong in-memory caching, storage, and persistence foundations, but **managed infrastructure, global scale, and vendor-supported SLAs** remain primarily commercial offerings.



---



**Made for platform engineers, application developers, and organizations seeking in-memory caching sovereignty.**  

Let's make in-memory caching more open, transparent, and performant.
