# CROSS-SILO MATHEMATICAL ISOMORPHISMS ⚠**CONTROL TEST**⚠ REPOSITORY

This is the ⚠**control**⚠ repository for the [cross-silo-structural-isomorphisms](https://github.com/ayresn/cross-silo-mathematical-isomorphisms) repository. Unlike that repository, entries within this repository were generated for a specific combination of user-supplied domains A and B, as a benchmark metric for comparison of successful structural isomorphism identification rates against that repository.

---

## PIPELINE STATUS AT A GLANCE
As of the current commit:

| Metric | Value |
| --- | --- |
| Total entries in dataset | 24 |
| Entries awaiting Stage 2 adversarial review | 0 |
| Entries that have completed Stage 2 adversarial review | 24 |
| — rejected at Stage 2 (`adversarial-rejected`) | **14 (58.3%)** |
| — advanced to Stage 3 queue (`adversarial-flagged`) | **10 (41.7%)** |
| — cleared with no reviewer objections (`adversarial-cleared`) | **0** |
| Entries that have completed Stage 3 human bibliometric validation | **0** |
| — failed bibliometric validation at Stage 3 (`failed-validation`) | **0** |
| — confirmed as novel, valid research leads (`validated-candidate`) | **0** |

---

## STAGE 2 YIELD BY GENERATING MODEL
Survival rate is the share of a model's entries that advanced to the Stage 3 queue rather than being rejected. Mean reject-vote share is the average across that model's entries of the fraction of panel reviewers voting REJECT. Both are computed over five entries per model, so all figures carry wide confidence intervals and none of the between-model differences should be treated as established.

| Model | Entries | Reviewed | Rejected | Survived | Mean reject-vote |
| --- | ---: | ---: | ---: | ---: | ---: |
| [Alibaba Qwen 3.8 Max](https://chat.qwen.ai/) | 2 | 2 | 0 | 100% | 44.4% |
| [Amazon Nova Pro](https://nova.amazon.com/) | 2 | 2 | 2 | 0% | 100.0% |
| [Anthropic Claude Opus 5](https://claude.ai/) | 2 | 2 | 1 | 50% | 38.9% |
| [Anthropic Claude Sonnet 5](https://claude.ai/) | 2 | 2 | 1 | 50% | 38.9% |
| [DeepSeek DeepSeek V4 Pro](https://chat.deepseek.com/) | 2 | 2 | 0 | 100% | 27.8% |
| [Google Gemini 3.1 Pro](https://aistudio.google.com/) | 2 | 2 | 0 | 100% | 22.2% |
| [Meta Muse Spark 1.1](https://www.meta.ai/) | 2 | 2 | 2 | 0% | 77.8% |
| [Microsoft Copilot 1.2](https://copilot.microsoft.com/) | 2 | 2 | 2 | 0% | 77.8% |
| [OpenAI GPT 5.6 Luna](https://chatgpt.com/) | 2 | 2 | 0 | 100% | 11.1% |
| [xAI Grok 4 Fast](https://grok.com/) | 2 | 2 | 2 | 0% | 83.3% |
| [Xiaomi MiMo V2.5 Pro](https://aistudio.xiaomimimo.com/) | 2 | 2 | 2 | 0% | 77.8% |
| [Z.AI GLM 5.2](https://chat.z.ai/) | 2 | 2 | 2 | 0% | 61.1% |
| **TOTAL** | **24** | **24** | **14** | **41.7%** | **55.1%** |