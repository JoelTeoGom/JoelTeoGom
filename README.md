<!-- ══════════════════════════════════════════════════════════════════════════════ -->
<!--  Theme: Terminal Dark  •  Accent: #00ff88  •  Author: Joel Teodoro            -->
<!-- ══════════════════════════════════════════════════════════════════════════════ -->

<div align="center">

### Joel Teodoro · Backend & Platform Engineer

**`Go`** · **`Distributed Systems`** · **`Kubernetes`** · **`Database Internals`**

<sub>Barcelona, Spain</sub>

<br>

<a href="mailto:joel.teodoro.software@gmail.com"><img src="https://skillicons.dev/icons?i=gmail" width="28" height="28" alt="Email"/></a>
&nbsp;&nbsp;
<a href="https://www.linkedin.com/in/joel-teodoro-gomez/"><img src="https://skillicons.dev/icons?i=linkedin" width="28" height="28" alt="LinkedIn"/></a>
&nbsp;&nbsp;
<a href="https://runtimerants.dev/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/chrome/chrome-original.svg" width="28" height="28" alt="Blog"/></a>

</div>

---

### `$ uname -a`

I run booking and payment systems in Go in production: hotels and buses, real traffic, real money.
On my own I rebuild the layers underneath, **Kubernetes** and **database internals**, until they stop
being magic, and I write it up at **[runtimerants.dev](https://runtimerants.dev)**. Preparing the CKA.

---

### `$ kubectl get pods -n lab`

```console
NAME                      READY   STATUS    WHAT
distributed-scheduler     1/1     Running   cron & at as a service, MySQL as the queue
kubernetes-from-scratch   1/1     Running   a small Kubernetes, written by hand
k8s-homelab               1/1     Running   kubeadm on bare metal, GitOps with Argo CD
pdfbox-aws                1/1     Running   serverless storage on AWS, all Terraform
go-key-affinity-lb        1/1     Running   1,000 requests → 4 backend calls
realtime-odds-platform    1/1     Running   ordered real-time fan-out over WebSockets
```

| Project | Why it's interesting |
| --- | --- |
| **[`distributed-scheduler`](https://github.com/JoelTeoGom/distributed-scheduler)** | Executors claim jobs with `SKIP LOCKED` and a lease; results commit only if a **fencing token** still matches, so a dead executor can never overwrite a reclaimed job. DLQ, history in Cassandra. Designed for ~1B executions/day. |
| **[`kubernetes-from-scratch`](https://github.com/JoelTeoGom/kubernetes-from-scratch)** | The node agent does what kubelet and kube-proxy do: a network namespace per pod, veth pairs, a bridge, and `KUBE-*` iptables chains that DNAT a service to a real pod. |
| **[`k8s-homelab`](https://github.com/JoelTeoGom/k8s-homelab)** | Three-node kubeadm cluster on KVM, Traefik with the Gateway API behind a Cloudflare Tunnel, GitOps from GitHub Actions to Argo CD. Every step documented with the why. |
| **[`pdfbox-aws`](https://github.com/JoelTeoGom/pdfbox-aws)** | File bytes never touch the backend: presigned S3 URLs, S3 events into SQS, an idempotent Lambda worker, an EventBridge sweeper. |
| **[`go-key-affinity-lb`](https://github.com/JoelTeoGom/go-key-affinity-lb)** | Key-affinity routing + per-node singleflight. Measured: **1,000 concurrent requests → 4 backend calls**, no distributed locks. |
| **[`realtime-odds-platform`](https://github.com/JoelTeoGom/realtime-odds-platform)** | Updates partitioned by `hash(eventId)` so each event stays ordered; a sharded WebSocket hub drops slow consumers instead of stalling the broadcast. |

<sub>Also: [`my-http-server`](https://github.com/JoelTeoGom/my-http-server) (HTTP over raw TCP) · [`go-hash-ring`](https://github.com/JoelTeoGom/go-hash-ring) · [`go-redis-token-bucket`](https://github.com/JoelTeoGom/go-redis-token-bucket) · notes in [`joel-software-notes`](https://github.com/JoelTeoGom/joel-software-notes)</sub>

---

### `$ cat stack.yml`

```yaml
go:       [grpc, graphql, rest, websockets, concurrency]
data:     [mysql, postgresql, redis, elasticsearch, cassandra, dynamodb]
infra:    [kubernetes, docker, gcp, cloud-run, aws, terraform, github-actions]
linux:    [namespaces, cgroups, netfilter/iptables]
design:   [hexagonal, event-driven, idempotency, outbox]
```

---

### `$ tail -n 4 ~/writing/log`

- **[From git push to a Running Pod](https://runtimerants.dev/posts/git-push-to-running-pod)**: nobody is orchestrating anything, just independent loops
- **[Your Database Writes Twice](https://runtimerants.dev/posts/write-ahead-log-internals)**: the write-ahead log, checkpoints, LSNs and CDC
- **[Go's HTTP Connection Pool](https://runtimerants.dev/posts/go-http-connection-pool)**: the key is the server, not the endpoint
- **[singleflight under a thundering herd](https://runtimerants.dev/posts/go-singleflight-internals)**: one hot key expires, N requests hit the DB

<sub>What I read and keep coming back to: [`software-engineering-guide`](https://github.com/JoelTeoGom/software-engineering-guide)</sub>

---

```console
$ echo $STATUS
open to backend and platform roles in Go · remote EU or Barcelona · joel.teodoro.software@gmail.com
```
