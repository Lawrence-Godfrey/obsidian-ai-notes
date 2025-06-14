## WebQA
- **What:** A **multimodal question answering** dataset.
- **Task:** Given a _question_ + _associated web image_, predict the _textual answer_.
- **Why it matters:** Tests a model’s ability to **reason jointly** over images _and_ external knowledge.
- **My take:** It’s a practical benchmark, but noisy — typical of "real-world web" messiness. Not the cleanest academic signal, but realistic.
---
## CIRR (Composable Image Retrieval with References)
- **What:** A **visual-only** retrieval dataset.    
- **Task:** Given a _reference image_ + a _textual modification_, retrieve the _correct target image_.
- **Example:** "Like this chair, but in blue."
- **Why it matters:** Forces a model to **understand nuanced visual/textual changes** — not just category matching.
- **My take:** I like CIRR — it stresses _fine-grained_ compositional reasoning, a real weakness in many vision models.
---
## FashionIQ
- **What:** **Fashion-specific image retrieval** benchmark.
- **Task:** Given a _fashion item image_ and a _textual description of the change_, retrieve the _desired fashion item_.
- **Example:** "Similar to this dress, but make it sleeveless and red."
- **Why it matters:** High stakes in real-world recommender systems (fashion e-commerce, etc.).
- **My take:** Narrow domain (only fashion), but extremely useful for studying fine-grained multimodal retrieval.

---
## ReMuQ (Retrieval of Multimodal Queries)
- **What:** A **retrieval benchmark** where queries are _both images and text_.
- **Task:** Given an _(image + text)_ query, retrieve matching _(image + text)_ candidates.
- **Why it matters:** **True multimodal retrieval** — both the query and candidates are complex, mixed-modal.
- **My take:** ReMuQ is exciting because it pushes retrieval closer to how humans think (we rarely use _only_ text or _only_ images).