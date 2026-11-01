# Optional: local models

Skip this unless you have data that must never leave your machine, want to run without per-call API charges while accepting hardware and electricity costs, or want to learn how agent harnesses work. Model quality and setup effort depend on the job and hardware. Evaluate a local setup on your own tasks before assigning unattended work.

The following results come from the reference-build account on an 8 GB GPU. Its evaluation logs are not included in this public kit, so treat the numerical results as reported observations, not independently reproduced benchmarks:

- **Instruction overhead mattered in this build.** One popular framework sends more than 10,000 tokens of fixed instructions and 30-plus tool definitions on every call, and users report 9B and 14B models crashing under it. A purpose-built loop with a fixed prompt of about 400 tokens left room for actual work.
- **Measure prompt processing as well as generation.** Agent prompts run to thousands of tokens while replies are short, so prompt processing dominates each step. Keep the fixed prompt byte-identical every turn so the model server can reuse its cache.
- **Smaller context ran faster and still passed.** A 9B model at 32K context passed the build's 10-task eval and ran about 46% faster than at 64K, because more of the model fit on the GPU.
- **Set the context length explicitly.** Ollama's current default depends on available VRAM. Set the context size for the job, inspect the running allocation with ollama ps, and check long-input behavior on your model. See the [official context guide](https://docs.ollama.com/context-length).
- **Turn reasoning off for routine steps.** With it on, both test models wrote 1,000 to 3,000 tokens of reasoning before short answers.
- **Code verifies, models don't.** The local model misreported a tool result. The build's harness checks every job's output itself, applies triage plans in code, and logs the result regardless of what the model claims.
- **Split the work.** Frontier agents write a plan of small steps, each with a check command. The local harness executes them one at a time on its own branch, never pushes, and a person reviews before merging.

If you add one, configure its runtime to load the shared rules and enforce the access limits. A rules file alone does not configure a harness: writes limited to `scratch/` and `agents/`, the model server bound to localhost only, and no access to your GitHub token except through an approval queue.

---

[Previous: Failure modes and guardrails](12-failure-modes.md) | [Contents](../README.md#contents) | [Next: Learning path](14-learning-path.md)
