# Diffbook

<img src="icon.png" width="96" alt="Diffbook icon, an open notebook with a green plus and minus">

Local-first macOS worklog for computational research. Daily notes, project folders, and summaries of what changed in your scripts and notebooks.

Diffbook is for computational researchers and scientists. It keeps a daily record of the work and summarizes the files you actually changed.

## Features

- Daily notebook, newest day first
- Projects and groups
- Local folders, whether or not they are git repositories
- Remote folders over SSH
- Change summaries for R, Python, shell, Markdown, and notebooks
- Optional local AI with Ollama, or your own API key
- In-app updates

## Install

Apple Silicon Mac, macOS 12 or later.

[Download the latest DMG](https://github.com/Cytewise/Diffbook/releases/latest)

Open the disk image and drag Diffbook into Applications.

## Plans

**Free.** No account. Daily notebook, projects, local folders, and summaries with Ollama or your own API key. Nothing is synced.

**Cloud, $9 a month.** Sync across your Macs: the notes, summaries, and project details described under Privacy. Ollama and your own API key still work.

**Cloud + AI, $18 a month.** Everything in Cloud, plus Ask DiffBook.

## Privacy

Diffbook does not require an account. Until you sign in, nothing is synced.

Local models run through Ollama on your Mac. That request is not sent to any AI company or to us. If you instead pick a cloud model and enter your own API key, that request goes to the provider you chose.

Cloud sync is optional. It stays off until you sign in on a Cloud plan. When it is on, daily notes and the written summaries are uploaded to our server. They are not end-to-end encrypted, so we can read them. The text of your scripts and notebooks is not uploaded. Diffbook syncs:

- Project and group names, descriptions, and the folder you connected (a local path or an `ssh://` address, not the files in that folder)
- Daily notes
- Day and project summaries (the summary text, not your source files)
- Which file paths you chose to track
- Ask conversations, if you use Ask

Diffbook does not sync file contents, file history, per-file diffs, SSH passwords, or API keys. A remote folder is read over SSH onto your Mac so it can be summarized there. Those bytes are not part of sync.

## This Mac

Apple Silicon (M1 or later) and macOS 12 or later. Diffbook itself does not need a separate graphics card.

The notebook and folder watching work without a local model. Summaries on this Mac use [Ollama](https://ollama.com), which uses the Mac’s own memory. A discrete GPU is not required. Rough memory estimates of some recommended models:

- About 4 GB of memory: `gemma3:1b`, `llama3.2:1b`, `deepseek-r1:1.5b` (downloads under about 1.5 GB)
- About 8 GB: `llama3.2`, `gemma3:4b`, `deepseek-r1:7b`
- About 16 GB: `gemma3:12b`, `deepseek-r1:14b`

Smaller models are the practical default. Larger ones are optional and slower on a machine without that much memory.

## Links

- [cytewise.com/diffbook](https://cytewise.com/diffbook/)
- [Changelog](CHANGELOG.md)
- [Releases](https://github.com/Cytewise/Diffbook/releases)
