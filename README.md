# Emacs CodeRabbit — AI Code Review Inside Emacs

`emacs4rabbit` brings [CodeRabbit](https://coderabbit.ai) directly into your Emacs workflow. Trigger AI-powered pull request reviews, browse inline comments, and act on suggestions — all without leaving your editor.

## Features

- Launch CodeRabbit reviews on any open PR from within Emacs
- Browse review threads in a dedicated `*coderabbit*` buffer
- Jump-to-file and apply suggested hunks with a single keybind
- Works with `magit`, `forge`, and standalone `git-commit` flows
- Supports GitHub, GitLab, and Bitbucket remotes

## Installation

```elisp
(use-package emacs4rabbit
  :after magit
  :config
  (setq emacs4rabbit-api-key "YOUR_CODERABBIT_API_KEY")
  (emacs4rabbit-mode 1))
```

## Quick Start

1. Open a PR in `magit` or `forge`
2. Run `M-x emacs4rabbit-review` (or bind it to a key)
3. CodeRabbit will analyze the diff and populate the `*coderabbit*` buffer
4. Navigate comments with `n`/`p`, apply suggestions with `RET`

## Configuration

| Variable | Default | Description |
|---|---|---|
| `emacs4rabbit-api-key` | `nil` | Your CodeRabbit API key |
| `emacs4rabbit-auto-review` | `nil` | Auto-trigger on `magit-push` |
| `emacs4rabbit-buffer-name` | `"*coderabbit*"` | Buffer name for reviews |
| `emacs4rabbit-review-depth` | `'full` | `'full` or `'summary` |

## Requirements

- Emacs 28+
- `magit` or `forge` (optional but recommended)
- CodeRabbit API key

# Watch the Demo

[emacs4rabbit — AI Code Review Inside Emacs](https://www.youtube.com/watch?v=DLzxrzFCyOs)
