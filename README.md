<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:13293d,100:00c2a8&height=200&section=header&text=AI%20Engineer&fontSize=60&fontColor=ffffff&fontAlignY=35&desc=LLM%20Applications%20%E2%80%A2%20ML%20Systems%20%E2%80%A2%20Full-stack%20AI&descAlignY=58&descSize=18" width="100%" />

<a href="https://github.com/tramslegend">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=3000&pause=900&color=00C2A8&center=true&vCenter=true&width=680&lines=AI+Engineer+%2F+Full-stack+Foundation;Building+LLM-powered+Applications;RAG%2C+Agents+%26+Tool-use+Pipelines;Studying+ML+from+First+Principles;From+Next.js+Products+to+AI+Systems" alt="Typing SVG" />
</a>

<br/>

![Focus](https://img.shields.io/badge/Focus-LLM_Applications-00c2a8?style=for-the-badge&labelColor=0d1117)
![Python](https://img.shields.io/badge/Python-ML_Tooling-3776AB?style=for-the-badge&labelColor=0d1117)
![TypeScript](https://img.shields.io/badge/TypeScript-Full--stack-3178C6?style=for-the-badge&labelColor=0d1117)
![Learning](https://img.shields.io/badge/Mode-Always_Shipping-f5a623?style=for-the-badge&labelColor=0d1117)

</div>

---

## `>` whoami

```python
class AIEngineer:
    background = "Full-stack TypeScript / Next.js engineer"
    now        = "Building AI-powered products & ML systems"
    building   = ["LLM apps", "RAG pipelines", "tool-using agents"]
    studying   = ["transformers from scratch", "autograd", "training loops"]
    stack_ml   = ["Python", "PyTorch", "LLM APIs", "vector DBs"]
    stack_web  = ["Next.js", "TypeScript", "Node.js", "Postgres", "Redis"]
    edge       = "I can take an AI idea from model to a shipped product"
    philosophy = "Understand the fundamentals, then ship real systems."
```

I come from **full-stack product engineering** — shipping real Next.js apps with payments, auth and
real-time systems — and I'm now focused on **AI engineering**: building **LLM-powered applications**
(RAG, agents, tool-use) and learning the ML foundations underneath by **implementing them from scratch**.

My edge: I don't just call a model API — I can wrap it in a real, production-grade product.

---

## `>` what I build

<table>
<tr>
<td width="33%" valign="top">

### 🤖 LLM Applications

RAG over private data<br/>
Tool-using agents<br/>
Structured output / function calls<br/>
Streaming chat UIs<br/>
Prompt & context engineering<br/>
Eval & guardrails<br/>
Cost / latency optimization

</td>
<td width="33%" valign="top">

### 🧠 ML Foundations

Transformers from scratch<br/>
Autograd & backprop<br/>
Training & fine-tuning loops<br/>
Tokenization & embeddings<br/>
Attention mechanics<br/>
Model evaluation<br/>
Scaling intuition

</td>
<td width="33%" valign="top">

### 🔌 Full-stack AI

Next.js + model backends<br/>
Vector DB integration<br/>
Streaming APIs & queues<br/>
Auth, billing & limits<br/>
Caching & rate limiting<br/>
Docker / Vercel deploys<br/>
Type-safe end to end

</td>
</tr>
</table>

---

## `>` the stack

<div align="center">

**AI / ML**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![Anthropic](https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=anthropic&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)

**AI App Layer**

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Vercel AI SDK](https://img.shields.io/badge/Vercel_AI_SDK-000000?style=flat-square&logo=vercel&logoColor=white)
![Vector DB](https://img.shields.io/badge/Vector_DB-pgvector_%2F_Pinecone-4169E1?style=flat-square&logo=postgresql&logoColor=white)

**Full-stack**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

</div>

---

## `>` a RAG pipeline

How I wire retrieval-augmented generation into a product:

```mermaid
flowchart LR
    A[User query] --> B[Embed query]
    B --> C{Vector search}
    C --> D[(Vector DB)]
    D --> E[Top-k chunks]
    E --> F[Build context + prompt]
    F --> G[LLM]
    G --> H[Stream answer + citations]
    H --> A
    G -.->|tool call| I[Functions / APIs]
    I -.-> F
```

---

## `>` from first principles

I learn by rebuilding the fundamentals, not just importing them. A micro-autograd in the spirit of backprop:

```python
class Value:
    """A scalar that tracks its gradient — the core idea behind autograd."""
    def __init__(self, data, _children=()):
        self.data, self.grad = data, 0.0
        self._backward = lambda: None
        self._prev = set(_children)

    def __mul__(self, other):
        out = Value(self.data * other.data, (self, other))
        def _backward():
            self.grad  += other.data * out.grad
            other.grad += self.data  * out.grad
        out._backward = _backward
        return out
```

<div align="center">

*Implementing transformers, autograd and training loops by hand — so the APIs aren't magic.*

</div>

---

## `>` currently

```
▸ Building   : my-autograd — a reverse-mode autodiff engine from scratch
▸ Studying   : GPT internals, attention, and training loops from first principles
▸ Next up    : vectorized Tensor engine, Adam optimizer, a small LLM app
```

---

## `>` featured

| Project | What it is | Highlights |
|---|---|---|
| **[my-autograd](https://github.com/tramslegend/my-autograd)** | A tiny reverse-mode autodiff engine + neural net library, pure Python, no frameworks | Implements backprop via topological-sort; trains an MLP from 48% → 96% accuracy |

<sub>The core of every ML framework (PyTorch's <code>loss.backward()</code>) built by hand to understand it end to end.</sub>

<!-- Add more real projects here as you build them. -->

---

## `>` platform capabilities

<details>
<summary><b>🤖 LLM Application Layer</b></summary>

- RAG over private documents with chunking + reranking
- Tool-using agents with structured (function-call) output
- Streaming chat with token-by-token UI
- Prompt / context engineering and templating
- Output validation and guardrails
- Token-cost and latency budgeting

</details>

<details>
<summary><b>🧠 ML Fundamentals (hands-on study)</b></summary>

- Transformer blocks: attention, MLP, residual, layernorm
- Autograd / backprop implemented by hand
- Training loops, optimizers, LR schedules
- Tokenization and embeddings
- Evaluation and overfitting diagnostics

</details>

<details>
<summary><b>🔌 Productionizing AI</b></summary>

- Next.js backends calling model providers
- Vector DB integration (pgvector / Pinecone)
- Streaming APIs, queues and background jobs
- Auth, rate limiting and usage metering
- Docker + Vercel deployment

</details>

---

## `>` engineering principles

```
1. Understand the fundamentals before importing the abstraction.
2. An LLM feature is still a product — auth, limits, errors, UX all matter.
3. Validate model output at the boundary; never trust it blindly.
4. Measure cost and latency like any other production metric.
5. Evals over vibes — know when the model actually got better.
6. Ship real systems, not notebooks.
```

---

## `>` role

<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=soft&color=0:0d1117,50:13293d,100:00c2a8&height=170&section=header&text=Building%20Intelligent%20Systems&fontSize=40&fontColor=ffffff&fontAlignY=40&desc=AI%20Engineer%20%E2%80%A2%20LLM%20Applications%20%E2%80%A2%20ML%20from%20First%20Principles&descSize=16&descAlignY=68" alt="AI Engineer banner" />

<br/><br/>

<img src="https://skillicons.dev/icons?i=python,pytorch,ts,react,nextjs,nodejs,docker&theme=dark" alt="stack" />

</div>

---

## `>` let's build

<div align="center">

Open to **AI engineering** roles and projects — LLM apps, RAG systems, and full-stack AI products.

<a href="https://github.com/tramslegend">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>
<!-- Add your real links, then uncomment:
<a href="mailto:you@example.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
<a href="https://linkedin.com/in/your-handle"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
-->

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00c2a8,50:13293d,100:0d1117&height=120&section=footer" width="100%" />

</div>
