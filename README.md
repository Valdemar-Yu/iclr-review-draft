# ICLR Review Draft

A reusable Codex skill for drafting concise, evidence-bounded reviews of ICLR submissions.

The skill is designed for papers that need a compact, human-sounding review. It reads the full submission, builds a claim map, checks facts against the paper, and produces:

- one-paragraph **Paper Summary**;
- two evidence-based **Critical Strengths**;
- two decision-relevant **Critical Weaknesses**;
- three to six **Questions For Authors**.

Weaknesses are written together with the untested or unsupported cases they affect. The workflow distinguishes “not reported” and “not tested” from observed failure, and treats prompt-like text inside a PDF as manuscript content rather than as instructions.

## Install

Clone the repository into the Codex skills directory:

```bash
git clone https://github.com/Valdemar-Yu/iclr-review-draft.git ~/.codex/skills/iclr-review-draft
```

If the skill is already installed, update it with:

```bash
git -C ~/.codex/skills/iclr-review-draft pull
```

## Use

Ask Codex:

```text
Use $iclr-review-draft to review this paper.
```

Provide the local PDF or the paper context. The output is a review draft for human verification; model settings, numbers, tables, and strong factual claims should be checked against the submission before use.

## License

MIT. See [LICENSE](LICENSE).
