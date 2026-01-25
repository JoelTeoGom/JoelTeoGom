<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->
<!--                                                                                        -->
<!--   ██████╗ ███████╗██╗   ██╗    ██████╗ ██████╗  ██████╗ ███████╗██╗██╗     ███████╗   -->
<!--   ██╔══██╗██╔════╝██║   ██║    ██╔══██╗██╔══██╗██╔═══██╗██╔════╝██║██║     ██╔════╝   -->
<!--   ██║  ██║█████╗  ██║   ██║    ██████╔╝██████╔╝██║   ██║█████╗  ██║██║     █████╗     -->
<!--   ██║  ██║██╔══╝  ╚██╗ ██╔╝    ██╔═══╝ ██╔══██╗██║   ██║██╔══╝  ██║██║     ██╔══╝     -->
<!--   ██████╔╝███████╗ ╚████╔╝     ██║     ██║  ██║╚██████╔╝██║     ██║███████╗███████╗   -->
<!--   ╚═════╝ ╚══════╝  ╚═══╝      ╚═╝     ╚═╝  ╚═╝ ╚═════╝ ╚═╝     ╚═╝╚══════╝╚══════╝   -->
<!--                                                                                        -->
<!--   Theme: Dark IDE   |   Accent: #00ff88   |   Author: Joel Teodoro                     -->
<!--                                                                                        -->
<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->

<div align="center">

<!-- ╔══════════════════════════════════════════════════════════════════════════════════╗ -->
<!-- ║                              PIXEL ART HEADER                                     ║ -->
<!-- ╚══════════════════════════════════════════════════════════════════════════════════╝ -->

```diff
+       ██╗ ██████╗ ███████╗██╗
+       ██║██╔═══██╗██╔════╝██║
+       ██║██║   ██║█████╗  ██║
+  ██   ██║██║   ██║██╔══╝  ██║
+  ╚█████╔╝╚██████╔╝███████╗███████╗
+   ╚════╝  ╚═════╝ ╚══════╝╚══════╝
```

<sub>Backend Engineer • Spain 🇪🇸</sub>

<br>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=14&duration=3000&pause=1000&color=00FF88&center=true&vCenter=true&repeat=true&width=450&lines=joel%40ide%3A~%24+echo+%22Building+things+that+scale%22;joel%40ide%3A~%24+go+run+distributed-systems.go;joel%40ide%3A~%24+kubectl+apply+-f+production.yml" alt="Typing SVG" />

<br><br>

<!-- ─────────────────────────────── SOCIAL ICONS (SVG only) ─────────────────────────────── -->

<a href="mailto:joel.teodoro.software@gmail.com">
  <img src="https://cdn.simpleicons.org/gmail/00ff88" width="28" height="28" alt="Email"/>
</a>
&nbsp;&nbsp;&nbsp;
<a href="https://www.linkedin.com/in/joel-teodoro-gomez/">
  <img src="https://cdn.simpleicons.org/linkedin/00ff88" width="28" height="28" alt="LinkedIn"/>
</a>
&nbsp;&nbsp;&nbsp;
<a href="https://joelteogom.github.io/">
  <img src="https://cdn.simpleicons.org/safari/00ff88" width="28" height="28" alt="Portfolio"/>
</a>

</div>

<br>

<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->

<p align="center">
<code>README.md</code> │ <code>terminal</code> │ <code>output</code>
</p>

<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->

### `joel@ide:~$ whoami`

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

<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->

### `joel@ide:~$ cat stack.yml`

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

<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->

### `joel@ide:~$ ps aux | grep focus`

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

<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->

### `joel@ide:~$ tree ~/projects --favorites`

<table>
<tr>
<td width="50%" valign="top">

```bash
# >_ cli-tools/
├── README.md
├── cmd/
└── internal/
```

**`>_` CLI Tools**

<sup>Small tools that solve real problems</sup>

Building utilities that automate the boring stuff.
If I do something twice, it becomes a script.
If I do it three times, it becomes a tool.

</td>
<td width="50%" valign="top">

```bash
# { } distributed/
├── README.md
├── consensus/
└── events/
```

**`{ }` Distributed Systems**

<sup>Learning by building</sup>

Experimenting with consensus algorithms,
event sourcing, and everything that can go
wrong in distributed environments (spoiler: everything).

</td>
</tr>
<tr>
<td width="50%" valign="top">

```bash
# /api apis/
├── README.md
├── handlers/
└── middleware/
```

**`/api` Backend APIs**

<sup>REST, gRPC, GraphQL</sup>

Designing APIs that developers actually enjoy
using. Documentation included, because past
me hates undocumented APIs.

</td>
<td width="50%" valign="top">

```bash
# ./lab playground/
├── README.md
├── experiments/
└── poc/
```

**`./lab` Playground**

<sup>Where ideas go to be tested</sup>

Random experiments, proof of concepts, and
"what if I try this?" projects. Most fail,
some become real tools.

</td>
</tr>
</table>

<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->

### `joel@ide:~$ curl -s api.joel.dev/links`

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
  <img src="https://cdn.simpleicons.org/gmail/00ff88" width="32" height="32" alt="Email"/>
</a>
&nbsp;&nbsp;&nbsp;&nbsp;
<a href="https://www.linkedin.com/in/joel-teodoro-gomez/">
  <img src="https://cdn.simpleicons.org/linkedin/00ff88" width="32" height="32" alt="LinkedIn"/>
</a>
&nbsp;&nbsp;&nbsp;&nbsp;
<a href="https://joelteogom.github.io/">
  <img src="https://cdn.simpleicons.org/safari/00ff88" width="32" height="32" alt="Portfolio"/>
</a>
</p>

<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->

### `joel@ide:~$ git log --stat`

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=joelteogom&show_icons=true&hide_border=true&bg_color=0d1117&title_color=00ff88&icon_color=00ff88&text_color=6e7681&ring_color=00ff88" width="400"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=joelteogom&layout=compact&hide_border=true&bg_color=0d1117&title_color=00ff88&text_color=6e7681" width="340"/>
</p>

<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->

<br>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=joelteogom&color=00ff88&style=flat-square&label=views" alt="Profile views"/>
</p>

<p align="center">
  <code>// TODO: write better commit messages</code>
</p>

<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->
<!-- EOF                                                                                    -->
<!-- ══════════════════════════════════════════════════════════════════════════════════════ -->
