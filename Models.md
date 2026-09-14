Models for Coding 9/2026:

| Rank | Model                       | Download | Context | M3 64GB | Coding | Agentic coding |
| ---- | --------------------------- | -------: | ------: | ------- | ------ | -------------- |
| 🥇   | **Qwen3.6 35B**             |    ~23GB |    256K | ⭐⭐⭐⭐⭐   | ⭐⭐⭐⭐⭐  | ⭐⭐⭐⭐⭐          |
| 🥈   | **Qwen3.8 27B**             |    ~18GB |    256K | ⭐⭐⭐⭐⭐   | ⭐⭐⭐⭐⭐  | ⭐⭐⭐⭐⭐          |
| 🥉   | **Qwen3-Coder-Next**        |    ~52GB |    256K | ⭐⭐⭐     | ⭐⭐⭐⭐⭐  | ⭐⭐⭐⭐⭐          |
| 4    | **North Mini Code 30B-A3B** |    ~19GB |   488K* | ⭐⭐⭐⭐⭐   | ⭐⭐⭐⭐⭐  | ⭐⭐⭐⭐⭐          |
| 5    | **Devstral Small 2 24B**    |    ~15GB |    384K | ⭐⭐⭐⭐⭐   | ⭐⭐⭐⭐½  | ⭐⭐⭐⭐⭐          |
| 6    | **Qwen3-Coder 30B-A3B**     |    ~19GB |    256K | ⭐⭐⭐⭐⭐   | ⭐⭐⭐⭐½  | ⭐⭐⭐⭐⭐          |
| 7    | **GLM-4.7-Flash 30B-A3B**   |    ~19GB |    198K | ⭐⭐⭐⭐⭐   | ⭐⭐⭐⭐½  | ⭐⭐⭐⭐½          |
| 8    | **GPT-OSS 20B**             |    ~14GB |    128K | ⭐⭐⭐⭐⭐   | ⭐⭐⭐⭐   | ⭐⭐⭐⭐½          |
| 9    | **Laguna XS 2.1**           |    ~20GB |    256K | ⚠️      | ⭐⭐⭐⭐⭐  | ⭐⭐⭐⭐⭐          |
| 10   | **Qwen3.5 35B**             |    ~24GB |    256K | ⭐⭐⭐⭐⭐   | ⭐⭐⭐⭐   | ⭐⭐⭐⭐           |
| 11   | DeepSeek-Coder-V2 16B       |        ~ |       — | ⭐⭐⭐⭐⭐   | ⭐⭐⭐½   | ⭐⭐⭐            |
| 12   | Qwen2.5-Coder 32B           |        ~ |       — | ⭐⭐⭐⭐⭐   | ⭐⭐⭐½   | ⭐⭐⭐            |
| 13   | Codestral 22B               |        ~ |       — | ⭐⭐⭐⭐⭐   | ⭐⭐⭐    | ⭐⭐⭐            |
| 14   | DeepCoder 14B               |        ~ |       — | ⭐⭐⭐⭐⭐   | ⭐⭐⭐    | ⭐⭐⭐            |
| 15   | CodeGemma                   |        — |       — | ⭐⭐⭐⭐⭐   | ⭐⭐     | ⭐⭐             |
| 16   | StarCoder2                  |        — |       — | ⭐⭐⭐⭐⭐   | ⭐⭐     | ⭐⭐             |
| 17   | CodeLlama                   |        — |       — | ⭐⭐⭐⭐⭐   | ⭐⭐     | ⭐⭐             |
Models for report writing 9/2026:

|Rank|Model|Role I'd give it|M3/64GB|
|---|---|---|---|
|🥇|**Qwen3.6 35B**|Best overall research + writing|Excellent|
|🥈|**Qwen3.8 27B**|Research, synthesis, long documents|Excellent|
|🥉|**GPT-OSS 20B**|Reasoning/analysis/second opinion|Excellent|
|4|**Qwen3.5 35B**|General research/writing|Excellent|
|5|**Gemma 3 27B**|Polished prose/summarization|Excellent|
|6|**DeepSeek-R1 32B**|Deep reasoning/analysis|Excellent|
|7|**Mistral Small 3.x 24B**|Writing/summarization|Excellent|
|8|**GLM-4.7-Flash**|Research/reasoning|Excellent|
Research and report writing pipeline:

```
                    SOURCES
                       │
       ┌───────────────┴───────────────┐
       │                               │
       ▼                               ▼
 Qwen3.8 27B                     Qwen3.6 35B
 Source extraction                Research
 Summarization                    Synthesis
       │                               │
       └───────────────┬───────────────┘
                       ▼
                 GPT-OSS 20B
                Critical review
                Find weak claims
                Find omissions
                       │
                       ▼
                  Qwen3.6 35B
                  Final report
                       │
                       ▼
                  Gemma 4 26B
                Editorial pass
                       │
                       ▼
               FINAL DOCUMENT
```

| Model             | Editorial quality | Technical preservation | Speed on M3/64GB | Long report |
| ----------------- | ----------------: | ---------------------: | ---------------: | ----------: |
| **Gemma 4 26B**   |             ★★★★★ |                  ★★★★½ |            ★★★★★ |       ★★★★★ |
| **Qwen3.6 35B**   |             ★★★★½ |                  ★★★★★ |             ★★★★ |       ★★★★★ |
| **Gemma 4 31B**   |             ★★★★★ |                  ★★★★★ |              ★★★ |       ★★★★★ |
| Gemma 3 27B       |              ★★★★ |                   ★★★★ |             ★★★★ |        ★★★½ |
| Mistral Small 24B |              ★★★★ |                   ★★★★ |            ★★★★★ |        ★★★★ |

Model stacks with M3 Mac:

| Priority | Model                | Job                               | Version I'd run       |
| -------- | -------------------- | --------------------------------- | --------------------- |
| 🥇       | **Qwen3.6 35B**      | Primary general model + coding    | `qwen3.6:35b`         |
| 🥈       | **Qwen3.8 27B**      | Research + synthesis              | `qwen3.8:27b-q8_0`    |
| 🥉       | **Gemma 4 31B**      | Report writing + final editing    | `gemma4:31b`          |
| 4        | **GPT-OSS 20B**      | Reasoning + skeptical review      | `gpt-oss:20b`         |
| 5        | **Qwen3-Coder-Next** | Difficult coding / agentic coding | `qwen3-coder-next`    |
| 6        | **North Mini Code**  | Fast coding agent                 | `north-mini-code-1.0` |

---
# 1. Qwen3.6 35B — my default model

```
ollama pull qwen3.6:35b
```

This would be the model I point most applications at by default.

Ollama's current 35B package is a **35.5B MoE model, Q4_K_M, about 23 GB**, with a **256K context window**. Ollama specifically emphasizes repository-level reasoning and agentic coding improvements.

### I'd use it for

- Python
- PowerShell
- Bash
- Azure/Entra scripts
- debugging
- architecture
- technical questions
- general reasoning
- initial report drafts
- analyzing technical documentation
- Claude Code / OpenCode

It's essentially your **Swiss Army knife**.

And Ollama directly supports:

```
ollama launch claude --model qwen3.6:35b
```

and:

```
ollama launch opencode --model qwen3.6:35b
```

### Why Q4 instead of Q8?

Normally I'd prefer more precision if memory permitted, but for this particular model I think the standard 23 GB Q4_K_M build is the right balance.

You want lots of memory left for:

**model + KV cache + macOS + IDE + browser + terminal + agent**

rather than consuming 40+ GB just on model weights.

For an interactive coding agent, speed matters too.

**Verdict: leave Qwen3.6 at Q4_K_M.**

---
# 2. Qwen3.8 27B Q8 — research model

This one I'd configure differently.

```
ollama pull qwen3.8:27b-q8_0
```

The regular model is roughly **18 GB**, but Ollama's Q8 version is about **30 GB**.

On a 32 GB Mac I'd use Q4.

On **your 64 GB Mac**, I'd take advantage of the additional RAM and use Q8 when the primary job is research and document analysis.

Ollama specifically describes Qwen3.8 as improving:

> coding, professional work, research, and long-horizon agentic tasks

and it supports **256K context**.

### I'd use Qwen3.8 for

- researching a security topic
- combining multiple sources
- summarizing documentation
- comparing vendor documentation
- analyzing long PDFs converted to text
- extracting findings
- developing research hypotheses
- building report outlines
- technical synthesis
- source-heavy research

For example:

```
Microsoft documentation
         +
CVE descriptions
         +
Security researcher blogs
         +
GitHub project
         +
Your testing notes
         ↓
    Qwen3.8
         ↓
Evidence / findings / conclusions
```

This is the model I'd make the **primary researcher**.

---
# Important RAM caveat with Qwen3.8 Q8

Don't combine Q8 with 256K context just because both are technically available.

I'd normally run:

### Ordinary research

**32K context**

### Large research project

**64K context**

### Very large document set

**128K context**

Only use 256K when there's an actual reason.

A 30 GB Q8 model plus a huge KV cache can consume a substantial fraction of your 64 GB unified memory.

If you routinely need 128–256K, switch to:

```
ollama pull qwen3.8:27b
```

The standard model is only about 18 GB.

So I'd think of it as:

**Q8 = maximum source-analysis quality**

**Q4 = maximum context/efficiency**

---
# 3. Gemma 4 31B — final report writer/editor

I've changed my mind slightly from my earlier recommendation.

For **your particular 64 GB machine**, I'd actually install the **31B dense Gemma 4** rather than 26B for final report writing.

```
ollama pull gemma4:31b
```

Gemma 4 31B is dense, while the 26B model is an MoE with roughly 4B active parameters. Both support native system prompts and are designed for reasoning, professional workloads, coding and multimodal work.

For interactive workloads I'd prefer the faster 26B MoE.

But editorial work isn't latency-sensitive in quite the same way.

If I'm going to give a model:

> "Here is my finished 35-page security assessment. Preserve every technical assertion, but improve clarity, structure, consistency and executive readability."

I'd rather give the job to the **31B dense model**.

### Gemma's job isn't research

This distinction is important.

I wouldn't tell Gemma:

> Research CVE-X and tell me what's going on.

I'd give it already researched material.

Its task would be:

```
Raw technical report
        ↓
   Gemma 4 31B
        ↓
• Cleaner language
• Consistent terminology
• Better transitions
• Reduced repetition
• Stronger executive summary
• More professional tone
• Better section organization
```

For Board-facing or executive-facing reports, that role is particularly valuable.

---
# 4. GPT-OSS 20B — adversarial reviewer

```
ollama pull gpt-oss:20b
```

This is not primarily your writer.

It's your **reviewer**.

The current Ollama package is around **14 GB**, supports **128K context**, tools, and configurable reasoning effort.

That's extremely comfortable on your Mac.

I'd use it after Qwen finishes research.

Give GPT-OSS the evidence and report and tell it something like:

> Act as a skeptical technical reviewer. Identify claims that aren't supported by the supplied evidence, logical leaps, contradictory statements, missing counterarguments, security implications that haven't been considered, and conclusions stated with too much certainty.

This gives you a second model family critiquing the first model.

That's important.

Having:

**Qwen → critique Qwen**

is less useful than:

**Qwen → GPT-OSS challenges Qwen**

Different model families can have different blind spots.

---
# 5. Qwen3-Coder-Next — heavy coding specialist

```
ollama pull qwen3-coder-next
```

This is the specialist I'd pull out when Qwen3.6 struggles with something difficult.

Ollama describes it explicitly as being optimized for **agentic coding workflows and local development**.

Think:

```
Qwen3.6
   ↓
"This problem is becoming difficult."
   ↓
Qwen3-Coder-Next
```

I'd use it for:

- large repository changes
- multi-file debugging
- difficult refactoring
- unfamiliar codebases
- long agentic coding sessions
- complex implementation work
- coding where several attempts have failed

It wouldn't be loaded constantly.

It's a **special-purpose tool**.

---
# 6. North Mini Code — fast coding agent

```
ollama pull north-mini-code-1.0
```

North Mini Code has an interesting architecture:

**30B total parameters**

but only approximately:

**3B active parameters**

per token.

Cohere designed it specifically for **agentic software engineering**, and Ollama supports tools/thinking.

That's attractive on Apple Silicon because you can get relatively sophisticated coding behavior without the inference cost of a dense 30B model.

I'd experiment with it for:

- quick edits
- repetitive coding
- fixing tests
- generating utilities
- shell scripting
- smaller repositories
- autonomous agent tasks

It could end up being your **fast Claude Code model**, while Qwen3-Coder-Next becomes the heavyweight.

---
# So each model gets one job

This is the important part.

Rather than thinking:

> Which LLM is best?

I'd treat the Mac like a little local AI workstation.

```
┌───────────────────────────────────────────┐
│           YOUR M3 / 64 GB MAC             │
├───────────────────────────────────────────┤
│                                           │
│ Qwen3.6 35B                               │
│ └── Default / Coding / General            │
│                                           │
│ Qwen3.8 27B Q8                            │
│ └── Research / Source Analysis            │
│                                           │
│ Gemma 4 31B                               │
│ └── Report Writing / Editing              │
│                                           │
│ GPT-OSS 20B                               │
│ └── Reasoning / Critical Review           │
│                                           │
│ Qwen3-Coder-Next                          │
│ └── Difficult Coding                      │
│                                           │
│ North Mini Code                           │
│ └── Fast Agentic Coding                   │
│                                           │
└───────────────────────────────────────────┘
```

There's remarkably little redundancy there.

---
