<!-- ══════════════════════════════════════════════════════════════════════════════ -->
<!--  Theme: Terminal Dark  •  Accent: #00ff88  •  Author: Joel Teodoro            -->
<!-- ══════════════════════════════════════════════════════════════════════════════ -->

<div align="center">

<img src="./assets/joel-wave.svg" width="450" alt="Joel Teodoro"/>

**`Backend Engineer`** · **`Go & Distributed Systems`** · **`Catalonia, Spain 🇪🇸`**

<br>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=14&duration=3000&pause=1000&color=00FF88&center=true&vCenter=true&repeat=true&width=560&lines=%24+go+test+-race+./...;%24+redis-cli+--eval+ratelimit.lua;%24+kubectl+rollout+status+deploy%2Fgateway" alt="Typing SVG" />
</a>

<br><br>

<a href="mailto:joel.teodoro.software@gmail.com">
  <img src="https://skillicons.dev/icons?i=gmail" width="32" height="32" alt="Gmail"/>
</a>
&nbsp;&nbsp;&nbsp;
<a href="https://www.linkedin.com/in/joel-teodoro-gomez/">
  <img src="https://skillicons.dev/icons?i=linkedin" width="32" height="32" alt="LinkedIn"/>
</a>
&nbsp;&nbsp;&nbsp;
<a href="https://runtimerants.dev/">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/chrome/chrome-original.svg" width="32" height="32" alt="Blog"/>
</a>

</div>

<br>

---

### `$ whoami`

```go
package main

import "fmt"

type Engineer struct {
    Name     string
    Role     string
    Location string
    Primary  string
    Focus    []string
}

func (e Engineer) String() string {
    return fmt.Sprintf("%s — %s, shipping %s to production", e.Name, e.Role, e.Primary)
}

func main() {
    me := Engineer{
        Name:     "Joel Teodoro",
        Role:     "Backend Engineer",
        Location: "Catalonia, Spain",
        Primary:  "Go",
        Focus: []string{
            "System design and the trade-offs nobody writes down",
            "Concurrency: goroutines, channels, sync primitives",
            "Real-time delivery: WebSocket fan-out, pub/sub, sharding",
            "Data layer internals: B+ trees, WAL, replication, CDC",
        },
    }

    fmt.Println(me)
    // Joel Teodoro — Backend Engineer, shipping Go to production
}
```

I work on booking platforms — hotels and buses. Payments, cancellations, refunds,
and third-party APIs that document one thing and return another. Go on Kubernetes,
real traffic, real money.

Most of what I know came from something breaking first. I write it down at
**[runtimerants.dev](https://runtimerants.dev)** so I don't have to learn it twice.

---

### `$ cat stack.yml`

```yaml
core:
  language:   go                # everything I ship
  apis:       [graphql, grpc, rest, websockets]
  data:       [mysql, postgresql, redis, elasticsearch]
  messaging:  [pub/sub, rabbitmq, kafka]

infrastructure:
  orchestration: [kubernetes, docker]
  cloud:         [gcp, cloud-run]
  ci_cd:         [gitlab-ci, github-actions]

architecture:
  - hexagonal / ports & adapters
  - domain-driven design
  - event-driven services
  - caching, and the harder half: invalidation

also_shipped:
  - java / spring-boot          # two years of it, same team. I wrote a post about it
  - python, c                   # tooling and systems coursework
```

---

### `$ ps aux | grep focus`

```diff
@@ right now @@

+ System design — ride-hailing, ticketing, real-time feeds. Designed properly,
+   not four boxes and an arrow labelled "queue"
+ Cassandra internals — LSM trees, partition keys, and the hot partition problem
+   that every tutorial forgets to mention
+ Redis past the cache — atomic Lua, pub/sub internals, distributed coordination
+ RabbitMQ ingest — sharded consumers, backpressure, delivery guarantees that hold

@@ reading @@

+ Concurrency in Go — Cox-Buday. Finished it, then read it again
+ Designing Data-Intensive Applications — Kleppmann. Halfway, no rush
```

---

### `$ tree ~/projects --favorites`

Small systems, each built to understand one specific failure mode. All of them run.

<table>
<tr>
<td width="50%">

**[`go-sharded-ws-hub`](https://github.com/JoelTeoGom/go-sharded-ws-hub)**
> Fan-out that survives slow clients

Sharded in-memory hub, one write pump per connection, non-blocking send. If a client
can't keep up it gets dropped — one slow consumer should never stall the broadcast.
Lock contention split across shards by `hash(eventID)`.

</td>
<td width="50%">

**[`go-redis-token-bucket`](https://github.com/JoelTeoGom/go-redis-token-bucket)**
> One limit, N nodes, no drift

Token bucket in Redis, enforced by an atomic Lua script. Redis being single-threaded
isn't a limitation here — it's the entire correctness guarantee.

</td>
</tr>
<tr>
<td width="50%">

**[`go-priority-scheduler`](https://github.com/JoelTeoGom/go-priority-scheduler)**
> Idle workers that actually sleep

Min-heap for ordering, `sync.Cond` for parking. Highest-priority job runs first and
nobody burns a core spinning on an empty queue.

</td>
<td width="50%">

**[`CrispLite`](https://github.com/JoelTeoGom/CrispLite)**
> Chat, end to end

WebSockets, Redis Pub/Sub for cross-instance delivery, Postgres for durability,
hexagonal all the way down. Built it to find out what breaks in a messaging system.
Plenty does.

</td>
</tr>
<tr>
<td width="50%">

**[`DDD-Ecommerce`](https://github.com/JoelTeoGom/DDD-Ecommerce)**
> Aggregates that defend themselves

Real bounded contexts (Order, Catalog), invariants enforced inside the aggregate
instead of in a service somewhere, domain events over a decoupled bus.

</td>
<td width="50%">

**[`my-http-server`](https://github.com/JoelTeoGom/my-http-server)**
> HTTP, parsed by hand

Request parsing, routing and responses written from scratch over raw TCP. The fastest
way I know to stop treating `net/http` as magic.

</td>
</tr>
</table>

<details>
<summary><b><code>./lab</code> — concurrency patterns, isolated and runnable</b></summary>

<br>

| Repo | What it does |
| --- | --- |
| [`go-errgroup-example`](https://github.com/JoelTeoGom/go-errgroup-example) | Parallel fetch, ordered results, bounded concurrency, first error wins |
| [`go-circuit-breaker-example`](https://github.com/JoelTeoGom/go-circuit-breaker-example) | The full `CLOSED → OPEN → HALF-OPEN` cycle against a downstream that keeps failing |
| [`go-fanout-race`](https://github.com/JoelTeoGom/go-fanout-race) | Fan out N requests, keep the fastest, cancel the rest |
| [`SingleFlight-Golang`](https://github.com/JoelTeoGom/SingleFlight-Golang) | Collapsing duplicate in-flight calls so a cache miss doesn't become a stampede |
| [`Snowflake-generator-service`](https://github.com/JoelTeoGom/Snowflake-generator-service) | 64-bit time-ordered IDs. Thread-safe, no collisions, no coordination |
| [`Data-structures`](https://github.com/JoelTeoGom/Data-structures) | The usual suspects, from scratch, with generics |

</details>

---

### `$ cat ~/writing/latest.md`

Deep dives from **[runtimerants.dev](https://runtimerants.dev)**. Long-form, with the
benchmarks and the source, because "it's faster" isn't an argument:

- **[The `context` Package](https://runtimerants.dev/posts/go-context-package-concurrency)** — cancellation across a concurrent call graph, from done channels up
- **[singleflight Internals](https://runtimerants.dev/posts/go-singleflight-internals)** — one hot key expires, N requests hit the DB. Here's how it collapses them
- **[Write-Ahead Log Internals](https://runtimerants.dev/posts/write-ahead-log-internals)** — what actually happens on INSERT, and how it ends up as CDC
- **[DB Indexes & Transactions](https://runtimerants.dev/posts/database-indexes-transactions-internals)** — B+ trees and row locks are the same story told twice
- **[Go vs Spring Boot](https://runtimerants.dev/posts/golang-vs-springboot)** — two years with both, same team, same infra, actual numbers

---

### `$ curl -s runtimerants.dev/api/links`

```json
{
  "blog":     "https://runtimerants.dev",
  "linkedin": "linkedin.com/in/joel-teodoro-gomez",
  "email":    "joel.teodoro.software@gmail.com",
  "status":   "open to backend / distributed systems roles — remote or Barcelona"
}
```

---

### `$ git log --stat`

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=joelteogom&show_icons=true&hide_border=true&bg_color=0d1117&title_color=00ff88&icon_color=00ff88&text_color=c9d1d9" width="420"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=joelteogom&layout=compact&hide_border=true&bg_color=0d1117&title_color=00ff88&text_color=c9d1d9" width="340"/>
</p>

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=joelteogom&color=00ff88&style=flat-square&label=views"/>
</p>

<p align="center">
  <code>// TODO: write better commit messages</code>
</p>
