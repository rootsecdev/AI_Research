If you were producing a security research report, I'd use the stack this way.

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

Code Flows Only

```
┌───────────────────────────────────────────┐
│           Coding Flow Tree                │
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
## Phase 1 — Gather evidence

Web search, Microsoft Learn, GitHub, CVEs, vendor documentation, your own testing, etc.

The LLM should **not** be trusted to manufacture the research sources.

---
## Phase 2 — Qwen3.8

Feed the collected sources into:

```
qwen3.8:27b-q8_0
```

Have it:

- extract claims
- summarize sources
- identify disagreements
- identify technical implications
- build a chronology
- separate observations from inference
- preserve citation/source identifiers

Result:

**structured research notes**

---
## Phase 3 — Qwen3.6

Then:

```
qwen3.6:35b
```

turns those findings into the actual technical report.

For example:

```
1. Executive Summary
2. Background
3. Technical Analysis
4. Attack Surface
5. Findings
6. Exploitability
7. Business Impact
8. Detection Opportunities
9. Mitigations
10. Recommendations
11. References
```

---
# Phase 4 — GPT-OSS attacks the report

Then:

```
gpt-oss:20b
```

gets:

**sources + findings + draft report**

and tries to tear it apart.

I'd specifically make it find:

- hallucinated claims
- weak evidence
- overstatement
- missing evidence
- alternative interpretations
- inconsistent conclusions
- technical errors
- duplicated findings
- unsupported severity ratings
- questionable remediation advice

This is basically your **peer reviewer**.

---
# Phase 5 — Qwen fixes it

Give the criticism back to:

```
qwen3.6:35b
```

along with the original sources.

Tell it to correct only problems justified by the critique/evidence.

Now you have the **technical final**.

---
# Phase 6 — Gemma 4 does the final editorial pass

Finally:

```
gemma4:31b
```

gets the finished report.

But I'd give Gemma a very restrictive system instruction:

> Do not introduce new facts, technical claims, recommendations, numbers, vulnerabilities, products, citations, or conclusions. Preserve the technical meaning. Your role is solely editorial: improve readability, organization, consistency, grammar, professional tone, transitions, and conciseness.

That's extremely important.

Otherwise an editorial LLM may decide to "improve" the report by adding information.

---
