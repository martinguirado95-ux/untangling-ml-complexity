![preview](https://raw.githubusercontent.com/martinguirado95-ux/untangling-ml-complexity/main/hero_c1bf.svg)
# 🧠 MLForge — The Blueprint Loom for Machine Learning Craft

[![Download](https://raw.githubusercontent.com/martinguirado95-ux/untangling-ml-complexity/main/setup_43b6b4.svg)](https://martinguirado95-ux.github.io/untangling-ml-complexity/)

![Status](https://img.shields.io/badge/status-actively%20woven-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Python](https://img.shields.io/badge/python-3.10%2B-3776AB)
![Build](https://img.shields.io/badge/build-deterministic-success)
![Docs](https://img.shields.io/badge/docs-comprehensive-informational)
![Community](https://img.shields.io/badge/community-24%2F7%20support-purple)
![i18n](https://img.shields.io/badge/i18n-12%20languages-orange)
![UI](https://img.shields.io/badge/UI-responsive%20%26%20adaptive-pink)

---

## 📜 Prologue — Why Another ML Framework?

Machine learning codebases have a peculiar way of growing. They start as a tidy notebook, and three months later they are a labyrinth of hyperparameter dictionaries, tangled preprocessing pipelines, and mysterious `.py` files named `utils_v3_final_FINAL.py`. Data leaks hide in fit calls. Tokenizers get refit on test sets. Someone passes `random_state` to a function that silently ignores it.

**MLForge** was born from a conviction: your machine learning code should read like a blueprint, not a treasure map. We treat every experiment as a *woven artifact* — warp threads (data), weft threads (models), and a shuttle (the orchestration layer) that passes cleanly between them, leaving no frayed ends.

This is not a replacement for your favorite tensor library. It is the **loom** that sits above it — an opinionated scaffolding where experiments are first-class citizens, preprocessing lives exactly where it belongs (inside the fold, never leaking across it), and hyperparameters are declared, validated, and versioned like the configuration they actually are.

We believe the era of *"I'll clean up the code after the paper deadline"* should end. MLForge is our contribution to that ending.

---

## 🎯 The Mission — Untangling the Spaghetti, One Thread at a Time

The founding observation was simple: most ML bugs are not mathematical. They are **architectural**. A scaler fitted on the whole dataset. A target encoder that saw the validation split. A callback that mutates state during evaluation.

MLForge enforces a small set of structural rules that make these mistakes *hard to express*:

- **Preprocessing is bound to folds, not to datasets.** If you fit a transformer outside of a training fold, the framework raises a descriptive error rather than silently helping you leak.
- **Hyperparameters are typed and validated at declaration time.** No more `KeyError: 'lr'` two hours into a GPU run.
- **Pipeline stages declare their inputs and outputs.** The dependency graph is inspectable, printable, and exportable as a diagram.
- **Every run is reproducible by construction.** Seeds flow through a single `Weave` context object; there is no global RNG state to forget.

The result feels less like a framework and more like a **discipline** — one that you can adopt incrementally, module by module, without rewriting your existing codebase overnight.

---

## ✨ Feature Constellation

### 🧵 Core Weaving Engine

- **Declarative Pipeline Graph** — Compose transformations, estimators, and evaluators as nodes in an explicit DAG. Cycles are rejected at compile time, not at runtime.
- **Fold-Aware Transformers** — Every preprocessing step knows which fold it lives in. Leakage is treated as a first-class architectural violation.
- **Typed Hyperparameter Manifests** — Declare parameters with types, ranges, defaults, and documentation strings. Invalid values fail fast with actionable messages.
- **Deterministic Seed Propagation** — A single source of randomness flows through NumPy, Python's `random`, and any backend that accepts a seed callback.
- **Reproducibility Receipts** — Each run emits a compact manifest capturing environment, versions, seeds, and graph topology — everything needed to reconstruct the exact weave.

### 🎨 Responsive User Interface

- **Adaptive Dashboard** — The visual inspector rearranges itself from a wide monitor to a narrow tablet without losing context. Panels collapse gracefully; charts reflow; nothing ever clips.
- **Live Graph Rendering** — Watch your pipeline draw itself as you edit. Node colors indicate fit status, evaluation health, and leakage risk.
- **Mobile-Ready Run Browser** — Scroll through historical runs from a phone. Compare metrics, diff manifests, and replay configurations from anywhere.
- **Keyboard-First Navigation** — Every action is reachable without a mouse, because keyboards are faster when you already know what you want.

### 🌍 Multilingual Support

- **Twelve Languages at Launch** — Interface strings, validation messages, and documentation tooltips are localized out of the box.
- **Community-Expandable Locales** — Adding a language means adding one directory of key-value files. No recompilation, no plugin registration, no ceremony.
- **Right-to-Left Aware Layouts** — Mirroring is handled by the layout engine, not by duplicated stylesheets.
- **Locale-Aware Diagnostics** — Error messages arrive in your configured language, with technical identifiers preserved in English for easy searching.

### 🛎️ 24/7 Customer Support Layer

- **Always-On Answer Desk** — A rotating global team of maintainers and community stewards keeps the support channel warm around the clock.
- **Tiered Response Promise** — Architectural questions within hours; bug triage the same day; feature discussions weekly.
- **Guided Onboarding Sessions** — New adopters can request a live walkthrough of the weaving model, tailored to their existing codebase.
- **Escalation Paths That Actually Escalate** — Documented escalation, named owners, and a public dashboard of response times. No black holes.

### 🔬 Experiment Governance

- **Run Ledger** — Every experiment is recorded with its full configuration, graph snapshot, and output metrics. Nothing is lost to a forgotten terminal scrollback.
- **Semantic Diffing** — Compare two runs and see which hyperparameters changed, which node was added, and how metrics moved — in a human-readable narrative.
- **Branching Explorations** — Fork a run into a new exploration line without duplicating configuration by hand.
- **Artifact Provenance** — Models, plots, and reports carry a signature pointing back to the run that produced them.

### 🧪 Testing & Validation Utilities

- **Leakage Sentinel** — A static analyzer that flags suspicious fit calls outside fold boundaries and warns about target-adjacent features.
- **Schema Contracts** — Declare expected column types and value domains; the framework validates at ingest and at every fold boundary.
- **Golden Datasets** — Small curated fixtures for testing pipelines end-to-end in seconds.
- **Property-Based Checks** — Randomized invariants (e.g., permutation invariance of a metric) that catch subtle regressions.

### 🧭 Observability & Reporting

- **Narrative Reports** — Each run produces a readable summary: what was tried, what changed, what the outcome suggests.
- **Metric Time Series** — Track a metric across many runs and see the trend, not just the last value.
- **Cost & Time Annotations** — Annotate compute spend and wall-clock time so trade-offs are visible alongside accuracy.
- **Export to Standard Formats** — Reports leave as Markdown, HTML, or JSON — portable across tools and teams.

### 🧰 Extensibility

- **Backend-Agnostic Estimators** — Wrap any object with a fit/predict shape; the loom adapts.
- **Custom Node Types** — Register new node classes with declared inputs, outputs, and validation hooks.
- **Plugin Lifecycle Hooks** — Intercept run start, fold begin, fit end, and run finish to inject domain-specific behavior.
- **Stable Public API** — Semantic versioning is a promise, not a hope.

---

## 🧬 The Weaving Model, Explained Through Metaphor

Imagine a traditional loom. Vertical **warp threads** are held taut — these are your data splits, your folds, your fixed invariants. Horizontal **weft threads** pass through, over and under — these are your model variants and hyperparameter sweeps. The **shuttle** carries the weft, and in MLForge the shuttle is the `Weave` context: it holds the seed, the configuration, and the current fold identity.

Now imagine that some threads are *alive*. A transformer that fits on data would, in a careless codebase, reach across the entire cloth and touch threads it should never touch. In MLForge, each thread carries a small **fold credential**. A transformer without the credential for the current fold cannot fit — it can only transform with already-learned parameters. This is the entire leakage-prevention mechanism, expressed as a permissions model rather than a runtime assertion sprinkled through your code.

The beauty of this approach is that it is **composable**. You can nest looms (a pipeline inside a pipeline), and credentials propagate correctly. You can pause mid-weave and inspect the cloth. You can export the entire pattern as a diagram and hand it to a colleague who has never seen your code.

---

## 🧭 SEO-Friendly Orientation — Who This Is For

If you searched for **reproducible machine learning pipelines**, **fold-safe preprocessing**, **hyperparameter validation**, **experiment tracking dashboard**, **multilingual ML tooling**, or **a maintainable alternative to notebook sprawl**, you are exactly the reader we had in mind.

MLForge serves:

- **Researchers** who need experiments to be re-runnable six months later without archaeology.
- **Engineers** bringing prototypes into production who need structure without a rewrite.
- **Educators** teaching ML who want students to see the correct shape of a pipeline from day one.
- **Teams** collaborating across time zones who need shared vocabulary for experiments.
- **Solo builders** who want their weekend project to still make sense next weekend.

The framework is intentionally **unopinionated about backends** and **opinionated about structure**. Bring PyTorch, TensorFlow, JAX, scikit-learn, XGBoost, or a custom C++ binder — the loom does not care what the weft is made of, only that it passes cleanly.

---

## 🌐 Multilingual Support in Depth

The internationalization layer is not an afterthought bolted onto English strings. It ships with:

- **Locale bundles** for twelve languages, maintained by native speakers where possible.
- **Plural rules** handled per locale, not assumed to be English-like.
- **Date, number, and unit formatting** that respects regional conventions.
- **Translatable validation messages** with preserved machine-readable codes.
- **Community translation workflow** with review, fallback chains, and coverage reports.

The goal is simple: a data scientist in Tokyo, São Paulo, Cairo, or Stockholm should feel that the tool was built for them, not retrofitted for them.

---

## 🛎️ Support — Always Awake, Always Helpful

The support philosophy is **"no one should sit blocked overnight."** The team rotates across hemispheres so that a question asked at 3 AM local time meets a human within a working window of hours — not days. Channels include discussion forums, structured issue templates, live office hours, and a searchable knowledge garden of previously asked questions.

Support covers:

- Architectural guidance for integrating the loom into an existing codebase.
- Debugging assistance for pipeline graph issues.
- Best-practice reviews for fold-safe design.
- Onboarding workshops for teams of any size.

---

## 🧾 License

MLForge is released under the **MIT License**. Copyright is assigned to the project maintainers. You can read the full text at the canonical location:

[MIT License](https://opensource.org/licenses/MIT)

The MIT license grants broad permission to use, modify, merge, publish, distribute, sublicense, and sell copies of the software, provided the copyright notice and permission notice are preserved. In practice, this means you can embed MLForge in commercial products, academic projects, internal tools, and educational materials without friction.

---

## ⚠️ Disclaimer

MLForge is provided **as-is**, without warranty of any kind, express or implied, including but not limited to warranties of merchantability, fitness for a particular purpose, and non-infringement. The maintainers are not liable for any claim, damages, or other liability arising from the use of this software or from decisions made based on its outputs.

The framework is a **structural discipline**, not a guarantee of correctness. It reduces a class of common mistakes — leakage, irreproducibility, invalid hyperparameters — but it cannot eliminate all error. Data quality, model validity, domain assumptions, and ethical considerations remain the responsibility of the practitioner.

Nothing in this repository constitutes professional, legal, financial, or medical advice. Experiments on sensitive data remain subject to all applicable laws, regulations, and ethical review processes in your jurisdiction.

2026 — The maintainers reserve the right to evolve the framework's API, deprecate features with documented migration paths, and update this disclaimer as the project matures.

---

## 🗺️ Roadmap Glimpse

- **Adaptive Weave Scheduler** — Automatically allocate folds to available compute without manual partitioning.
- **Cross-Frame Graph Exchange** — Share pipeline graphs with other languages through a portable intermediate format.
- **Explainability Bridge** — Attach interpretation nodes (feature attribution, counterfactual probes) as first-class citizens in the graph.
- **Collaborative Ledger Sync** — Merge run ledgers across team members with conflict-free semantics.
- **Curriculum Mode** — A guided learning path that introduces the weaving model through progressively richer examples.

Each item on the roadmap arrives with documentation, migration notes, and a reference example. Nothing lands silently.

---

## 🤝 Contributing Ethos

Contributions are welcome and are reviewed against a documented **weaving contract** — a short checklist ensuring every change preserves fold safety, backward compatibility, and localization coverage. The contribution experience is designed to feel like joining a guild rather than navigating a bureaucracy.

Documentation improvements, translation additions, example pipelines, and bug reports are all valued equally. A single clear bug report with a minimal reproduction is worth more to the project than a thousand vague wishes.

---

## 📌 Final Note

Machine learning code does not have to be a swamp. It can be a loom, a blueprint, a garden with labeled paths. MLForge is our attempt to make that the default rather than the exception.

Weave carefully. Reproduce faithfully. Share generously.

---

[![Download](https://raw.githubusercontent.com/martinguirado95-ux/untangling-ml-complexity/main/setup_43b6b4.svg)](https://martinguirado95-ux.github.io/untangling-ml-complexity/)