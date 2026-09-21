# BoltAI for PopClip

Send selected text from any Mac app to BoltAI with two small PopClip extensions. Requires BoltAI 2.17.0 or later and PopClip 2026.8.1 (build 6221) or later.

- **BoltAI Workflows** opens the workflow picker with the selected text. Choose a workflow to run it with your saved prompt, model, preview, and output settings.
- **Ask BoltAI** opens Instant Chat with the selection as an editable attachment. Add your question and press Send when ready.

The extensions are independent. Install either or both from the [PopClip Extensions Directory](https://www.popclip.app/extensions/) once published. For local testing, download or clone this repository and open the `.popclipext` packages in `source/` with PopClip.

If you have both the website and Setapp editions of BoltAI installed, open each extension's PopClip settings and set **Open with** to the edition you want. The default follows macOS's `bolt://` handler.

## Privacy

Clicking either action passes the selected plain text to the BoltAI app on your Mac through its `bolt://` URL handler. The extensions do not contact a server or start an AI request themselves. If you run a workflow or send an Instant Chat message, BoltAI may send that text to the AI provider selected in your BoltAI settings. Review your workflow and provider settings before submitting sensitive text.

AI Workflows require Accessibility permission in BoltAI. The extension hands selected text to BoltAI; the workflow still uses its own configured input and output behavior.

## Support

Report extension issues in this repository's [GitHub Issues](https://github.com/BoltAI/popclip-extensions/issues). For BoltAI app support, visit [boltai.com](https://boltai.com).

## Publishing

The PopClip Directory reads the two source packages in `source/` when a version tag beginning with `v` is pushed. Keep package paths and identifiers stable after the first submission. The extensions use their own versions, separate from BoltAI app versions.

1. Install the [PopClip Directory GitHub app](https://github.com/apps/popclip-directory) for this repository only.
2. Test both extensions in PopClip with the released BoltAI app: app running and quit, multiline and Unicode selections, Ask's editable attachment and manual Send, and Workflow preview and direct output back into the source app. The BoltAI integration notes record a cold-launch focus issue for Ask BoltAI; do not submit that package until a real PopClip test confirms Instant Chat opens correctly.
3. Commit and push these files. Tag that commit `v1.0.0` and push the tag. PopClip uses the tag as the extension version.
4. Check the tagged commit's PopClip **Submission Check**. PopClip reviews successful submissions before publication. A later update needs a higher tag; moving an existing tag does not resubmit it.

See [PopClip's submission guide](https://www.popclip.app/extensions/submit) for the current process.
