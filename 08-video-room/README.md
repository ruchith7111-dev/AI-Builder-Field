# 08 · Video room

This is the repository's visual walkthrough area. It is designed for **actual playable media**, not a directory of YouTube URLs.

## Playback status

<blockquote>
<strong>No playable video assets have been uploaded yet.</strong><br/>
The connected GitHub writer can commit Markdown and SVG assets, but it cannot upload a binary MP4 attachment to GitHub's media host. A video filename or external YouTube URL would not create the inline player requested here, so no fake player is shown.
</blockquote>

GitHub supports video uploads in MP4, MOV, and WebM formats. For inline playback in Markdown, the media must be uploaded as a GitHub-hosted attachment. The recommended broadly compatible codec is H.264. See GitHub's [attaching files documentation](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/attaching-files).

## Planned walkthroughs

| Clip | Target length | Learning outcome | Status |
|---|---:|---|---|
| 01 · From vague prompt to implementation plan | 2–3 min | Turn a broad request into acceptance criteria and a small build plan | Script ready; media not uploaded |
| 02 · Debugging with evidence | 2–3 min | Reproduce, isolate, test one hypothesis, and verify the fix | Script ready; media not uploaded |
| 03 · How a RAG answer is actually produced | 3–4 min | See ingestion, retrieval, reranking, generation, and citation boundaries | Script ready; media not uploaded |

## How to add a genuinely playable clip

1. Export a short MP4 using H.264 video and AAC audio.
2. Keep the file below the limit shown by GitHub for the account and repository.
3. Edit this README or a file in this folder on GitHub.com.
4. Drag the video into the Markdown editor and let GitHub upload it.
5. Place the generated GitHub attachment URL on its own line in the relevant clip section.
6. Save and preview the rendered README. Confirm playback while signed out or in a separate browser for this public repository.

Do not use a YouTube iframe: GitHub strips iframe embeds from repository Markdown. Do not use an external video host as a video element source; GitHub's content policy may block it.

## Why no external video links?

The goal of this section is to let readers watch a walkthrough in the repository. A clickable thumbnail is useful in some READMEs, but it is not inline playback and is deliberately not presented here as a video.

## Production notes

The scripts and shot lists are in [video-production-notes.md](video-production-notes.md). They are designed to be recorded as screen walkthroughs with captions and narration.
