# Optional: local models

Skip this unless you have data that must never leave your machine, want unlimited background runs at no marginal cost, or want to learn how agent harnesses work. Frontier models are far better at agent work, and a local setup takes weeks of tuning.

What the reference build learned running a local agent on a laptop with an 8 GB GPU:

- **Off-the-shelf agent frameworks are too heavy for small models.** One popular framework sends more than 10,000 tokens of fixed instructions and 30-plus tool definitions on every call, and users report 9B and 14B models crashing under it. A purpose-built loop with a fixed prompt of about 400 tokens left room for actual work.
- **Reading speed matters more than writing speed.** Agent prompts run to thousands of tokens while replies are short, so prompt processing dominates each step. Keep the fixed prompt byte-identical every turn so the model server can reuse its cache.
- **Smaller context ran faster and still passed.** A 9B model at 32K context passed the build's 10-task eval and ran about 46% faster than at 64K, because more of the model fit on the GPU.
- **Set the context length explicitly.** Ollama runs at a 4,096-token default unless told otherwise, and truncates silently.
- **Turn reasoning off for routine steps.** With it on, both test models wrote 1,000 to 3,000 tokens of reasoning before short answers.
- **Code verifies, models don't.** The local model misreported a tool result. The build's harness checks every job's output itself, applies triage plans in code, and logs the result regardless of what the model claims.
- **Split the work.** Frontier agents write a plan of small steps, each with a check command. The local harness executes them one at a time on its own branch, never pushes, and a person reviews before merging.

If you add one, it's one more agent under the same rules file: writes limited to `scratch/` and `agents/`, the model server bound to localhost only, and no access to your GitHub token except through an approval queue.

---

[Previous: Failure modes and guardrails](12-failure-modes.md) | [Contents](../README.md#contents) | [Next: Learning path](14-learning-path.md)
