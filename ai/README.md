# AI & NLP (planned)

**Owner:** M1.

This planned module covers Arabic conversation, structured intent recognition, reviewed-content RAG, prompt engineering, and response evaluation. It is a guided practice companion, not unrestricted conversation, diagnosis, therapy, or authority. No AI application or model code has been scaffolded yet.

Represent input with fields such as message, intended communication goal, input modality, confidence, scenario ID, and clarification-needed state. Do not infer diagnoses or hidden emotional states. Low-confidence/ambiguous input should trigger a simple clarification or visual choices. The deterministic activity engine owns scenario sequence, allowed responses, safety rules and completion; use an LLM only for constrained interpretation/language generation within those boundaries.

Use only original or appropriately licensed content, with age band, skill goal, source/license, reviewer status, version and use restrictions. Chunk by activity/guidance unit, retrieve approved material, constrain output, and record content/model/prompt versions and references for reproducibility. Specialist review is required before activities or response boundaries enter a content pack. Use synthetic examples; CI must not call live model providers or require secrets.
