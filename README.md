<!-- ══════════════════════════════════════════════════════════════════════════════ -->
<!--  Theme: Terminal Dark  •  Accent: #00ff88  •  Author: Joel Teodoro            -->
<!-- ══════════════════════════════════════════════════════════════════════════════ -->

<div align="center">

<img src="./assets/joel-wave.svg" width="450" alt="Joel Teodoro"/>

**`Go`** · **`Distributed Systems`** · **`Kubernetes`** · **`Database Internals`**

<sub>Backend Engineer · Catalonia, Spain 🇪🇸</sub>

<br>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=14&duration=3000&pause=1000&color=00FF88&center=true&vCenter=true&repeat=true&width=560&lines=%24+ip+netns+exec+pod-a+curl+10.0.0.2%3A8080;%24+iptables+-t+nat+-L+PREROUTING+-n;%24+kubectl+get+nodes+-o+wide;%24+go+test+-race+.%2F..." alt="Typing SVG" />
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

### `$ uname -a`

```console
joel-teodoro 24.0-go #1 SMP PREEMPT backend distributed-systems x86_64 GNU/Linux
```

I build booking platforms in Go: hotels and buses, real traffic, real money.
What I enjoy is opening the layers underneath. Right now that means **Kubernetes**
(CKA on the way) and **database internals**. This GitHub is where I rebuild things
from scratch until they stop being magic, and **[runtimerants.dev](https://runtimerants.dev)**
is where I write down what broke along the way.

> 📚 **[`software-engineering-guide`](https://github.com/JoelTeoGom/software-engineering-guide)**
> The articles, blogs and books that shaped how I think about software, each with what I took from it.

---

### `$ cat /proc/joel/status`

```yaml
Name:      joel-teodoro
State:     R (running)            # backend in production, every day
Lang:      go                     # everything I ship
Layer:     application → kernel   # currently descending
Focus:     linux · networking · kubernetes · storage engines
Signals:   SIGTERM ignored        # graceful shutdown, obviously
```

---

### `$ lsmod | grep focus`

```console
Module              State       Notes
linux_internals     loaded      namespaces, cgroups: a container is just a process with opinions
netfilter           loaded      iptables, conntrack, DNAT/SNAT: how a ClusterIP actually gets routed
kubernetes          loaded      control plane, reconciliation loops, CNI, kube-proxy · CKA in progress
storage_engines     loading     pages, B+ trees vs LSM, WAL, MVCC: everything ends up on disk
```

---

### `$ kubectl get pods -n lab`

Building the things I use, from scratch, until they stop being magic.

```console
NAME                      READY   STATUS    AGE
kubernetes-from-scratch   1/1     Running   building
pdfbox-aws                1/1     Running   shipped
my-http-server            1/1     Running   shipped
go-key-affinity-lb        1/1     Running   shipped
go-sharded-ws-hub         1/1     Running   shipped
```

<table>
<tr>
<td colspan="2">

**[`kubernetes-from-scratch`](https://github.com/JoelTeoGom/kubernetes-from-scratch)**
> A toy Kubernetes, written by hand

A control plane, node agents and an L4 load balancer in front, talking over a protocol
of their own. The agent does what kubelet and kube-proxy do: pod lifecycle, network
namespaces, veth pairs, a node bridge, and `KUBE-*` iptables chains that DNAT a service
address to a real pod. Nothing wraps an existing tool.

</td>
</tr>
<tr>
<td width="50%">

**[`pdfbox-aws`](https://github.com/JoelTeoGom/pdfbox-aws)**
> File bytes never touch the backend

Serverless multi-tenant storage: Go on Lambda, DynamoDB for metadata, uploads straight
to S3 with presigned URLs. S3 events into SQS with a DLQ, an EventBridge-scheduled sweeper
over a sparse GSI. All Terraform.

</td>
<td width="50%">

**[`my-http-server`](https://github.com/JoelTeoGom/my-http-server)**
> HTTP, parsed by hand

Request parsing, routing and responses written from scratch over raw TCP. The fastest
way I know to stop treating `net/http` as magic.

</td>
</tr>
<tr>
<td width="50%">

**[`go-key-affinity-lb`](https://github.com/JoelTeoGom/go-key-affinity-lb)**
> 1000 concurrent requests, 4 backend calls

Key-affinity routing plus singleflight on each node. Neither works alone: affinity puts
every request for a key on the same node, singleflight collapses them there.

</td>
<td width="50%">

**[`go-sharded-ws-hub`](https://github.com/JoelTeoGom/go-sharded-ws-hub)**
> Fan-out that survives slow clients

Sharded in-memory hub, one write pump per connection, non-blocking send. A client that
can't keep up gets dropped. One slow consumer should never stall the broadcast.

</td>
</tr>
</table>

---

### `$ cat stack.yml`

```yaml
core:
  language:   go
  apis:       [graphql, grpc, rest, websockets]
  data:       [mysql, postgresql, redis, elasticsearch]
  messaging:  [pub/sub, rabbitmq, kafka]

infrastructure:
  orchestration: [kubernetes, docker]
  cloud:         [gcp, cloud-run, aws]
  aws:           [lambda, api-gateway, dynamodb, s3, sqs, eventbridge, iam]
  iac:           [terraform]
  ci_cd:         [gitlab-ci, github-actions]
  linux:         [namespaces, cgroups, netfilter/iptables]

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

### `$ ls -la ~/archive`

<details>
<summary><b>Earlier builds: Go concurrency and system design, one failure mode per repo</b></summary>

<br>

| Repo | What it does |
| --- | --- |
| [`go-redis-token-bucket`](https://github.com/JoelTeoGom/go-redis-token-bucket) | One rate limit across N nodes, enforced by an atomic Lua script |
| [`go-hash-ring`](https://github.com/JoelTeoGom/go-hash-ring) | Consistent hashing with virtual nodes, every number measured |
| [`go-priority-scheduler`](https://github.com/JoelTeoGom/go-priority-scheduler) | Min-heap ordering, `sync.Cond` parking, no idle spinning |
| [`CrispLite`](https://github.com/JoelTeoGom/CrispLite) | Chat end to end: WebSockets, Redis Pub/Sub, Postgres, hexagonal |
| [`DDD-Ecommerce`](https://github.com/JoelTeoGom/DDD-Ecommerce) | Bounded contexts and aggregates that enforce their own invariants |
| [`go-errgroup-example`](https://github.com/JoelTeoGom/go-errgroup-example) | Parallel fetch, bounded concurrency, first error wins |
| [`go-circuit-breaker-example`](https://github.com/JoelTeoGom/go-circuit-breaker-example) | Full `CLOSED → OPEN → HALF-OPEN` cycle against a failing downstream |
| [`go-fanout-race`](https://github.com/JoelTeoGom/go-fanout-race) | Fan out N requests, keep the fastest, cancel the rest |
| [`SingleFlight-Golang`](https://github.com/JoelTeoGom/SingleFlight-Golang) | Collapsing duplicate in-flight calls so a cache miss isn't a stampede |
| [`Snowflake-generator-service`](https://github.com/JoelTeoGom/Snowflake-generator-service) | 64-bit time-ordered IDs, no coordination |
| [`Data-structures`](https://github.com/JoelTeoGom/Data-structures) | The usual suspects, from scratch, with generics |

</details>

---

### `$ cat ~/reading/now`

```diff
+ Database Internals            Petrov       in progress
+ Designing Data-Intensive Apps Kleppmann    halfway, no rush
+ Concurrency in Go             Cox-Buday    read it twice
```

The full list lives in the guide linked above.

---

### `$ tail -n 5 ~/writing/log`

Deep dives from **[runtimerants.dev](https://runtimerants.dev)**, with the benchmarks
and the source, because "it's faster" isn't an argument:

- **[Write-Ahead Log Internals](https://runtimerants.dev/posts/write-ahead-log-internals)**: what actually happens on INSERT, and how it ends up as CDC
- **[DB Indexes & Transactions](https://runtimerants.dev/posts/database-indexes-transactions-internals)**: B+ trees and row locks are the same story told twice
- **[singleflight Internals](https://runtimerants.dev/posts/go-singleflight-internals)**: one hot key expires, N requests hit the DB
- **[The `context` Package](https://runtimerants.dev/posts/go-context-package-concurrency)**: cancellation across a concurrent call graph
- **[Go vs Spring Boot](https://runtimerants.dev/posts/golang-vs-springboot)**: two years with both, same team, actual numbers

---

### `$ dig +short joel.contact`

```json
{
  "blog":     "https://runtimerants.dev",
  "linkedin": "linkedin.com/in/joel-teodoro-gomez",
  "email":    "joel.teodoro.software@gmail.com",
  "status":   "open to backend / platform / distributed systems roles, remote or Barcelona"
}
```

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=joelteogom&color=00ff88&style=flat-square&label=views"/>
</p>

<p align="center">
  <code>// TODO: write better commit messages</code>
</p>
