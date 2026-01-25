<!-- ═══════════════════════════════════════════════════════════════════════════════ -->
<!-- IDE: GitHub Profile • Theme: Dark • Author: Joel Teodoro                       -->
<!-- ═══════════════════════════════════════════════════════════════════════════════ -->

<div align="center">

```

     ╭──────────────────────────────────────────────────────────────────────────╮
     │                                                                          │
     │        ▀▀█ █▀▀█ █▀▀ █                                                    │
     │          █ █  █ █▀▀ █                                                    │
     │       █▄▄█ ▀▀▀▀ ▀▀▀ ▀▀▀                                                  │
     │                                                                          │
     │       // Backend Engineer • Spain 🇪🇸                                    │
     │                                                                          │
     ╰──────────────────────────────────────────────────────────────────────────╯

```

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=14&duration=3000&pause=1000&color=00FF88&center=true&vCenter=true&repeat=true&width=435&lines=%24+echo+%22Building+things+that+scale%22;%24+go+run+distributed-systems.go;%24+kubectl+apply+-f+production.yml" alt="Typing SVG" />

<br>

<!-- ─────────────────────────────── SOCIAL ICONS ─────────────────────────────── -->

<a href="mailto:joel.teodoro.software@gmail.com"><img src="https://img.shields.io/badge/%20-0d1117?style=flat-square&logo=gmail&logoColor=6e7681" height="28"/></a>&nbsp;
<a href="https://www.linkedin.com/in/joel-teodoro-gomez/"><img src="https://img.shields.io/badge/%20-0d1117?style=flat-square&logo=linkedin&logoColor=6e7681" height="28"/></a>&nbsp;
<a href="https://joelteogom.github.io/"><img src="https://img.shields.io/badge/%20-0d1117?style=flat-square&logo=safari&logoColor=6e7681" height="28"/></a>

</div>

<br>

<!-- ═══════════════════════════════════════════════════════════════════════════════ -->

<table align="center"><tr><td>
<sub>&nbsp;&nbsp;📁 README.md&nbsp;&nbsp;</sub>
</td><td>
<sub>&nbsp;&nbsp;terminal&nbsp;&nbsp;</sub>
</td><td>
<sub>&nbsp;&nbsp;output&nbsp;&nbsp;</sub>
</td></tr></table>

<!-- ═══════════════════════════════════════════════════════════════════════════════ -->

### `$ whoami`

```go
package main

import "fmt"

type Developer struct {
    Name      string
    Role      string
    Location  string
    Languages []string
    Interests []string
}

func (d Developer) String() string {
    return fmt.Sprintf("%s — %s from %s", d.Name, d.Role, d.Location)
}

func (d Developer) CurrentlyLearning() string {
    return "Always something new in distributed systems"
}

func main() {
    me := Developer{
        Name:      "Joel Teodoro",
        Role:      "Backend Engineer",
        Location:  "Spain 🇪🇸",
        Languages: []string{"Go", "Java", "Python", "C"},
        Interests: []string{
            "Scalable microservices",
            "Event-driven architectures",
            "Making things faster",
            "Breaking things to understand them",
        },
    }

    fmt.Println(me)
    // Output: Joel Teodoro — Backend Engineer from Spain 🇪🇸
}
```

<sub>▸ go run whoami.go</sub>

<!-- ═══════════════════════════════════════════════════════════════════════════════ -->

### `$ cat stack.yml`

```yaml
# ─────────────────────────────────────────────────────────────
# stack.yml — current toolbox
# ─────────────────────────────────────────────────────────────

backend:
  primary:
    - go          # current obsession
    - java        # spring boot ecosystem
  secondary:
    - python      # scripting & automation
    - c           # when i need to go low-level

frameworks:
  - spring-boot   # enterprise stuff
  - gin           # fast & lightweight
  - grpc          # service communication

infrastructure:
  containers: [docker, kubernetes]
  messaging:  [kafka, rabbitmq]
  databases:  [postgresql, redis, mongodb]

practices:
  - clean-architecture
  - domain-driven-design
  - event-sourcing
  - test-driven-development
```

<sub>▸ cat ~/.config/stack.yml</sub>

<!-- ═══════════════════════════════════════════════════════════════════════════════ -->

### `$ ps aux | grep focus`

```diff
@@ current focus @@

+ Building microservices with Go — obsessed with performance & simplicity
+ Deep diving into Kafka internals — event streaming is beautiful
+ Kubernetes patterns — making deployments boring (in a good way)
+ System design — preparing for scale before it's needed

@@ actively avoiding @@

- Premature optimization (learning to resist)
- Writing code without tests (never again)
```

<sub>▸ ps aux | grep -E "(focus|avoid)" --color=always</sub>

<!-- ═══════════════════════════════════════════════════════════════════════════════ -->

### `$ tree ~/projects --favorites`

<table>
<tr>
<td width="50%" valign="top">

```
📂 cli-tools/
├── README.md
├── cmd/
└── internal/
```

**`>_` CLI Tools**

<sub>Small tools that solve real problems</sub>

Building utilities that automate the boring stuff.
If I do something twice, it becomes a script.
If I do it three times, it becomes a tool.

</td>
<td width="50%" valign="top">

```
📂 distributed/
├── README.md
├── consensus/
└── events/
```

**`{ }` Distributed Systems**

<sub>Learning by building</sub>

Experimenting with consensus algorithms,
event sourcing, and everything that can go
wrong in distributed environments (spoiler: everything).

</td>
</tr>
<tr>
<td width="50%" valign="top">

```
📂 apis/
├── README.md
├── handlers/
└── middleware/
```

**`/api` Backend APIs**

<sub>REST, gRPC, GraphQL</sub>

Designing APIs that developers actually enjoy
using. Documentation included, because past
me hates undocumented APIs.

</td>
<td width="50%" valign="top">

```
📂 playground/
├── README.md
├── experiments/
└── poc/
```

**`./lab` Playground**

<sub>Where ideas go to be tested</sub>

Random experiments, proof of concepts, and
"what if I try this?" projects. Most fail,
some become real tools.

</td>
</tr>
</table>

<sub>▸ tree ~/projects -L 2 --dirsfirst</sub>

<!-- ═══════════════════════════════════════════════════════════════════════════════ -->

### `$ curl -s api.joel.dev/links`

```json
{
  "email": "joel.teodoro.software@gmail.com",
  "linkedin": "linkedin.com/in/joel-teodoro-gomez",
  "portfolio": "joelteogom.github.io",
  "status": "open to interesting conversations"
}
```

<p align="center">
  <a href="mailto:joel.teodoro.software@gmail.com">
    <img src="https://img.shields.io/badge/%20-0d1117?style=for-the-badge&logo=gmail&logoColor=00ff88" alt="Gmail"/>
  </a>
  <a href="https://www.linkedin.com/in/joel-teodoro-gomez/">
    <img src="https://img.shields.io/badge/%20-0d1117?style=for-the-badge&logo=linkedin&logoColor=00ff88" alt="LinkedIn"/>
  </a>
  <a href="https://joelteogom.github.io/">
    <img src="https://img.shields.io/badge/%20-0d1117?style=for-the-badge&logo=safari&logoColor=00ff88" alt="Portfolio"/>
  </a>
</p>

<sub>▸ curl -s api.joel.dev/links | jq .</sub>

<!-- ═══════════════════════════════════════════════════════════════════════════════ -->

### `$ git log --stat`

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=joelteogom&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=00ff88&icon_color=00ff88&text_color=6e7681" width="400"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=joelteogom&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=00ff88&text_color=6e7681" width="340"/>
</p>

<sub>▸ git log --oneline --graph --all | head -20</sub>

<!-- ═══════════════════════════════════════════════════════════════════════════════ -->

<br>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=joelteogom&color=00ff88&style=flat-square&label=views" alt="Profile views"/>
</p>

<p align="center">
  <sub><code>// TODO: write better commit messages</code></sub>
</p>

<!-- ═══════════════════════════════════════════════════════════════════════════════ -->
<!-- EOF                                                                             -->
<!-- ═══════════════════════════════════════════════════════════════════════════════ -->
