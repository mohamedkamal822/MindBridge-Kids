# Sign recognition (research module)

**Owner:** M2.

Agree on a small supported Egyptian Sign Language vocabulary with a qualified ESL advisor; this is not full sign-language translation. Audit dataset provenance, consent/usage terms, labels, signer count, recording conditions and licenses before processing. Evaluate MediaPipe hand landmarks and a Random Forest baseline, split by signer, then compare temporal models only if needed. Report class balance, per-class precision/recall, macro-F1, confusion matrix, abstention, latency and battery; compare desktop performance with TFLite on target devices. Low-confidence/unsupported signs must abstain and offer retry or AAC.

Recognition should run on device where feasible. Camera mode needs a clear active indicator and is opened only after a just-in-time permission request. Never store or upload raw video; a future service fallback, if separately justified and reviewed, may accept landmark vectors only. TFLite export is stretch work and cannot block the text-first MVP. Record verified license terms and attribution before data use or redistribution; do not put restricted datasets/model artifacts in Git.
