# Hi, I'm Raza 👋

**Working where machine learning meets the hardware it runs on.**

I'm a CS student at the University of Massachusetts Amherst interested in **GPU computing, ML systems, and performance engineering**. I like understanding not only what a workload does, but what happens when it actually meets the machine underneath it.

I currently split my time across two roles:

* **Undergraduate Researcher, ML4Ed Lab** — building evaluation pipelines for LLM-generated scientific writing, with a focus on **grounding, citation use, and failure analysis**.
* **AI/Software Engineering Intern, Commonwealth of Massachusetts (EOTSS)** — building a multimodal search system over ~100K ecological-restoration images on AWS, spanning **VLM tagging, event-driven ingestion, natural-language search, and geospatial metadata enrichment**.

**The throughline: I like going one layer down.**

That has increasingly meant moving from using ML systems to understanding what sits underneath them: **implementing models from first principles, benchmarking memory-access patterns, and studying how the same computation behaves differently across hardware.**

🏆 **Wins:** HackUMass XIII · Hack(H)er413
🔭 **Currently:** transformers from scratch · CUDA kernels · ML infrastructure

## Featured Work

### 🧠 [Transformer From Scratch](https://github.com/GeekyMS/PersonalTransformer)

A decoder-only transformer built progressively across **NumPy → C++ → CUDA** to understand what deep-learning frameworks normally hide.

The NumPy implementation includes the full forward pass, a **hand-derived backward pass**, AdamW training, and generation, with every gradient checked against a PyTorch reference. I'm currently rebuilding the model in C++ around a hand-rolled tensor representation, **arena allocator**, and **tape-based autograd system**, validating each operation against the NumPy implementation before moving on.

The eventual goal is to take the same model into CUDA and understand attention from the hardware upward: **memory traffic, arithmetic intensity, tiling, and online softmax**, and why FlashAttention falls naturally out of those constraints.

*C++ · Python · NumPy · Autograd · Transformers · CUDA*

### ⚡ [CUDA & Performance](https://github.com/GeekyMS/CUDA-learning)

A from-first-principles exploration of how parallel algorithms interact with the hardware underneath them.

I started with CPU implementations to establish baselines before moving workloads onto CUDA. In matrix multiplication, changing **memory access and cache blocking** improved throughput from **2.21 → 6.26 GFLOP/s (~2.8×)**. Prefix scan produced the more interesting result: a theoretically parallel Blelloch implementation was substantially slower than sequential execution on CPU because **synchronization and increasingly strided memory accesses** overwhelmed the available parallelism.

The project uses those results as a starting point for understanding how the tradeoffs change with GPU execution, including **warps, coalescing, shared memory, reductions, and tiled kernels**.

*C++ · CUDA · Parallel Algorithms · Cache Locality · Performance Benchmarking*

### 🔐 DataVault — Winner, HackUMass XIII

A privacy-preserving RAG system for natural-language querying over sensitive data.

DataVault combines **encrypted storage with retrieval-augmented generation** while minimizing plaintext persistence, allowing users to search private records without treating the underlying database as an unrestricted source of readable data.

*Python · Docker · PostgreSQL · RAG*

## What I'm Interested In

I'm especially interested in systems where understanding the workload **and** the machine underneath it matters:

* GPU programming and memory behavior
* ML systems and infrastructure
* High-performance C/C++
* Parallel and distributed systems
* Model evaluation and reliability

## Connect

[LinkedIn](https://linkedin.com/in/razaalaqaband) · [razaalaqaband.com](https://razaalaqaband.com)

## 🛠️ Languages & Tools

<p align="left"><em>Systems &amp; Compute</em></p>
<p align="left">
<a href="https://isocpp.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="C++" width="40" height="40"/></a>
<a href="https://www.cprogramming.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="C" width="40" height="40"/></a>
<a href="https://developer.nvidia.com/cuda-zone" target="_blank" rel="noreferrer"><img src="https://img.shields.io/badge/CUDA-76B900?logo=nvidia&logoColor=white" alt="CUDA" height="33"/></a>
<a href="https://www.python.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python" width="40" height="40"/></a>
<a href="https://www.linux.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="Linux" width="40" height="40"/></a>
</p>

<p align="left"><em>ML &amp; Data</em></p>
<p align="left">
<a href="https://numpy.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/numpy/numpy-original.svg" alt="NumPy" width="40" height="40"/></a>
<a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/></a>
<a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"><img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit-learn" width="40" height="40"/></a>
<a href="https://www.postgresql.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg" alt="PostgreSQL" width="40" height="40"/></a>
<a href="https://www.mysql.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="MySQL" width="40" height="40"/></a>
</p>

<p align="left"><em>Infrastructure &amp; Cloud</em></p>
<p align="left">
<a href="https://aws.amazon.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="AWS" width="40" height="40"/></a>
<a href="https://www.docker.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg" alt="Docker" width="40" height="40"/></a>
<a href="https://git-scm.com/" target="_blank" rel="noreferrer"><img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="Git" width="40" height="40"/></a>
</p>

<p align="left">
<sub>AWS: Lambda · SQS · API Gateway · Aurora · Bedrock · CDK</sub>
</p>

<p align="left"><em>Web</em></p>
<p align="left">
<a href="https://react.dev/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="React" width="40" height="40"/></a>
<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="JavaScript" width="40" height="40"/></a>
<a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="HTML" width="40" height="40"/></a>
<a href="https://flask.palletsprojects.com/" target="_blank" rel="noreferrer"><img src="https://cdn.simpleicons.org/flask/white" alt="Flask" width="35" height="35"/></a>
</p>
