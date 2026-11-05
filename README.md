# Clairacte

**Local transcription and a professional French drafting workspace.**

This public repository contains installers and end-user guidance. Development source and some linked engineering/security guides are private and require authorized access.

Clairacte helps a French *commissaire de justice* organize matters, transcribe recordings, prepare factual reports, review documents and export professional files. It was designed around the needs of a practice in Mérignac, Gironde. The interface and professional documents are in French; developer documentation is in English.

**Created and maintained by [BeanQ (@B3ANQ)](https://github.com/B3ANQ).** The development repository retains its original name, **Transcriptor**; the application is distributed as **Clairacte**.

[Downloads](#downloads) · [Installation](#installation) · [Quick start](#quick-start) · [How it works](#how-it-works) · [Privacy](#privacy-and-data) · [Development](#development) · [Documentation](#documentation)

## Downloads

Choose the installer for your computer. Both downloads are public and require no GitHub account.

| Platform | Direct download | Version and status | Release details |
| --- | --- | --- | --- |
| macOS Apple Silicon, ARM64 | [Download Clairacte for Mac (.dmg)](https://github.com/B3ANQ/Clairacte-Releases/releases/download/v0.6.1-mac-preview/Clairacte-0.6.1-mac-arm64.dmg) | **0.6.1 — Mac preview**, locally built and verified | [Notes and checksums](https://github.com/B3ANQ/Clairacte-Releases/releases/tag/v0.6.1-mac-preview) |
| Windows, x64 | [Download Clairacte for Windows (.exe)](https://github.com/B3ANQ/Clairacte-Releases/releases/download/v0.5.1-windows-legacy/Clairacte-0.5.1-win-x64.exe) | **0.5.1 — latest verified Windows installer**, older version | [Notes and checksums](https://github.com/B3ANQ/Clairacte-Releases/releases/tag/v0.5.1-windows-legacy) |

**Windows 0.6.1 is not available yet.** The Windows download does not include the 0.6 update interface or the 0.6.1 recovery/export fixes. An Intel Mac or Linux installer is not currently provided.

The Mac preview is ad hoc signed without Apple Developer ID/notarization, and the Windows installer is unsigned. Operating-system verification or publisher warnings can appear. Current verification results and remaining dependencies are documented in the [0.6.1 completion report](https://github.com/B3ANQ/Transcriptor/blob/main/docs/18-local-quality-verification.md).

Download the `.dmg` or `.exe`, rather than GitHub's **Source code** archives. The Mac `.zip` attached to its release is an updater archive. Installer files live in the public [Clairacte-Releases repository](https://github.com/B3ANQ/Clairacte-Releases); development source remains private.

## Installation

### macOS

1. Download the Apple Silicon `.dmg` above.
2. Quit an existing Clairacte installation and retain an encrypted backup before upgrading.
3. Open the disk image and drag **Clairacte** into **Applications**.
4. Eject the disk image, then launch Clairacte from Applications.
5. Allow microphone access when you choose to record an observation.

The current build can be blocked by Gatekeeper because publisher signing is not configured. See the [macOS trust and signing guide](https://github.com/B3ANQ/Transcriptor/blob/main/docs/10-macos-trust-and-signing.md) for the precise status; do not disable system protections globally.

### Windows

1. Download the x64 `.exe` above.
2. Quit an existing installation and retain an encrypted backup before upgrading.
3. Run the installer, select the installation folder and complete the French setup wizard.
4. Launch Clairacte from its installed shortcut.

Windows may display an unsigned-publisher or reputation warning. This download is the previously verified **0.5.1** build; see its release notes before choosing it for your workflow.

### Before professional use

Set your office identity and preferred terminology in **Paramètres**, choose light, dark or system appearance, and enable **Définir un mot de passe** for independent vault protection. Keep the password safely: the application cannot recover forgotten vault or backup passwords. Test your own equipment and representative documents before relying on a new installation.

## Quick start

1. **Create or open a matter.** Use **Nouveau dossier** with a title, or **Importer un enregistrement** from the dashboard to create a matter automatically. Administrative details can be completed later.
2. **Add your sources.** Under **Observations & audio**, type/paste observations, import text, import audio or record a short note. Distinguish personal observations, attributed declarations and documentary information.
3. **Transcribe and review.** Choose **Transcrire cet audio**, then **Relire la transcription**. Listen back, correct names, figures and uncertain passages, and choose **Conserver comme source**.
4. **Prepare the document.** Open **Rédaction**, select the appropriate mode and edit directly. Optional AI assistance creates a proposal for review and acceptance. **État des lieux** provides room sections and equipment lists.
5. **Check and export.** Use the separate **Relecture** workflow, inspect **Aperçu et export**, then export DOCX or PDF. Retain an encrypted backup through **Paramètres**.

### Importing a 90-minute recording

No special folder is required. Choose **Observations & audio → Importer un audio**, select the file wherever it is stored, then click **Transcrire cet audio** beside it.

- Supported imports: MP3/MPEG/MPGA, WAV, M4A/MP4, WebM, OGG and FLAC.
- Limits: **2 GiB per imported file** and **four hours for transcription**. A 1 h 30 recording is supported.
- Long recordings are prepared and recognized in local parts. You can pause and explicitly resume completed work.
- The encrypted original, raw transcription and editable working copy remain distinct.
- Direct microphone capture is intended for short notes; import longer recordings made with your usual recording application.

The default speech model is included in the installer. No API key, subscription, separate FFmpeg installation or manual audio splitting is needed. Processing time depends on the computer and recording. The test fixture covers a 90-minute file with a short spoken segment followed by silence; continuous 90-minute professional speech accuracy has not been benchmarked.

For transcript-only export, copy the reviewed working transcription into the document editor and use **Aperçu et export**. No further AI request is necessary. See the [complete user guide](https://github.com/B3ANQ/Transcriptor/blob/main/docs/04-user-guide.md).

## Features

| Area | Available workflow |
| --- | --- |
| Matters | Search, references, contacts, addresses, intervention details, status and archive |
| Sources | Typed/pasted/imported notes, preserved originals, attributed declarations and room associations |
| Audio | Encrypted originals, playback/seeking, local transcription, progress, pause/resume and explicit review |
| Photographs | Import, preview, captions, ordering, room links and selection for export |
| Factual reports | Editable proposals from supplied observations, source comparison and uncertainty warnings |
| Property condition reports | Room-by-room coverings, joinery, equipment bullets and apparent defects; no automatic example equipment |
| Drafting modes | Applicant-first-person requests, letters, instruments and professional communications |
| Correction and review | Separate minimal-correction and critical-review modes, targeted suggestions and acceptance controls |
| Editing | Headings/lists, native undo/redo, autosave status, version history/restoration and clipboard copy |
| Templates and office settings | Reusable structures, visible placeholders, preferred terminology and office identity |
| Exports and backups | DOCX/PDF, selected numbered/captioned photographs, encrypted workspace/matter backup and restoration |
| Legal research | A structured notebook with manually recorded primary-source links and consultation details |
| Appearance | Light, dark and system themes, keyboard navigation and visible processing/error states |

Writing, correction, critical-review and image AI assistance require the optional local writing service described below. Ordinary editing, deterministic room composition, saved-file access and transcription work without it. Legal research is **not automatically verified**: a saved source URL does not validate a citation or legal conclusion.


## How it works

Clairacte keeps source material separate from the working document. The original observation or recording is retained while the user reviews a transcription, an edited copy or an AI proposal.

Audio is prepared by a bundled, network-disabled **FFmpeg** build and transcribed on the computer by **[whisper.cpp](https://github.com/ggml-org/whisper.cpp)**. The installer includes multilingual speech weights and voice-activity detection. Recordings are not uploaded to a transcription provider.

Optional text/image assistance uses an installed **[Ollama](https://ollama.com/)** model through the fixed local endpoint `127.0.0.1:11434`. Each drafting mode has its own instructions and output contract, based on the [immutable French professional requirements](https://github.com/B3ANQ/Transcriptor/blob/main/docs/authoritative-fr.txt). Profiles instruct the model to preserve facts, names, dates, amounts, terminology and descriptive order, and to separate declarations from personal observations.

Substantive proposals require user acceptance. These controls support review; they do not establish the truth of an observation or guarantee that a model will never invent, omit or misinterpret information. Final professional judgment remains with the user.

### Optional local writing assistant

1. Install and start **[Ollama](https://ollama.com/download)** separately.
2. In **Paramètres**, choose **Actualiser la disponibilité**.
3. Install the suggested **Qwen3-VL 4B** local model through the application, or select an already installed compatible local model. The suggested download is approximately 3.3 GB.
4. Return to **Rédaction**, select a mode and request a proposal.

Keep Ollama configured for local operation. Cloud models and redirects are rejected by Clairacte. After installation, compatible cached models can run offline while Ollama is available. Its memory, storage and performance requirements depend on the chosen model and hardware; no minimum-hardware certification is claimed. See [Ollama's local-operation guidance](https://docs.ollama.com/faq).

### Cost and connectivity

| Operation | Processing and requirements |
| --- | --- |
| Editing, organization, room composition and exports | Local; available offline |
| Default transcription | Local; bundled engine/models; no provider fee or account |
| Optional writing/image assistance | Local Ollama service/model; no paid fallback |
| Model/software downloads and update checks | Internet access; explicit downloads |
| Opening legal research links | External browser; source access depends on the relevant website |

**No paid transcription account or API key is required.** Local processing uses the user's hardware, storage, time and electricity. GitHub's hosted builds have [separate usage allowances and potential charges](https://docs.github.com/en/billing/concepts/product-billing/github-actions). Publisher-signing services can also have costs; see [Development](#development).

## Privacy and data

Matters, documents and recordings are stored locally by default. The vault uses platform encryption; an optional independent password adds protection and locking. Long audio originals are encrypted separately from the main vault. Source originals are not silently overwritten by corrections or accepted proposals.

| Data | Storage or handling |
| --- | --- |
| macOS workspace | Normally `~/Library/Application Support/etude-workspace/` |
| Windows workspace | Normally `%APPDATA%\etude-workspace\` |
| Vault and retained audio | Encrypted application data; legacy storage name retained across branding/upgrades |
| Backups | Encrypted export with a separately chosen backup password |
| Final DOCX/PDF and clipboard | Plaintext output; protect the destination and any external copies |
| Ollama processing | Separate local process; its memory, logs, storage and swap are outside the vault |
| Update checks | Public GitHub release metadata; no matter, document or recording is transmitted |

Use the in-app backup workflow when transferring to another computer/account; copying only `workspace.vault` can omit retained audio. The application cannot recover a forgotten password. Uninstalling normally retains user data. Deleting a matter does not erase independent exports, backups, OS copies or guarantee physical erasure.

Read the [security policy](https://github.com/B3ANQ/Transcriptor/blob/main/SECURITY.md), [threat model](https://github.com/B3ANQ/Transcriptor/blob/main/docs/07-security-assessment.md) and [current local-processing data flow](https://github.com/B3ANQ/Transcriptor/blob/main/docs/13-free-local-workspace.md). No regulatory compliance, professional-secrecy guarantee or security certification is claimed.

## Updates and release status

The 0.6 application includes French update controls under **Paramètres → Mises à jour de Clairacte**. It checks a fixed public repository and validates signed manifests, versions, platform, sizes and hashes before accepting a download. Downloads and installation require explicit action; installation waits for saving and refuses active recording/processing.

Existing 0.5.x installations need one manual updater-enabled upgrade. The current Mac release is a **prerelease**, excluded from the stable update feed. A complete stable Windows/Mac release is still held, so the preview can report the stable feed as unavailable. Automatic public publishing and trusted native replacement also depend on the required publishing/signing credentials. See the [update and signing operations guide](https://github.com/B3ANQ/Transcriptor/blob/main/docs/16-updates-and-trusted-distribution.md).

## Verification

**Latest recorded verification: 5 November 2026, on macOS Apple Silicon.**

- All **14 local verification stages passed**, including **66 automated tests**, with zero failed/skipped.
- The full runtime/development dependency audit reported **zero known vulnerabilities at that time**.
- The Mac 0.6.1 DMG/ZIP passed integrity checks; actual installation, launch and bundled French transcription passed in an isolated profile.
- Both pages of each representative DOCX/PDF were rendered and visually reviewed, including accents, equipment bullets, page breaks and selected photographs/captions.
- A real local-model correction was checked separately; this is a sample, not a general AI-accuracy benchmark.

Windows **0.6.1** installation/uninstallation and real signed native update replacement remain unverified. The downloadable Windows **0.5.1** has its own earlier verification record. Publisher credentials and a Windows execution environment are still required for a complete current two-platform release. Automated primary-source legal-citation verification is not implemented.

See the [detailed 0.6.1 report](https://github.com/B3ANQ/Transcriptor/blob/main/docs/18-local-quality-verification.md), [machine-readable results](https://github.com/B3ANQ/Transcriptor/blob/main/docs/qa-061-results.json) and [earlier 0.5.1 platform record](https://github.com/B3ANQ/Transcriptor/blob/main/docs/15-release-051-verification.md). Tests cover controls and representative fixtures; they do not prove universal factual/legal correctness or absence of unknown security defects.

## Development

Development is maintained in the private [Transcriptor source repository](https://github.com/B3ANQ/Transcriptor). Authorized contributors can find native setup, build, test and contribution instructions there. End users only need an installer and the optional local writing service described above. This public distribution repository does not publish the private development checkout.

## Documentation

- [Current Mac release notes and checksums](https://github.com/B3ANQ/Clairacte-Releases/releases/tag/v0.6.1-mac-preview).
- [Detailed recorded verification results](https://github.com/B3ANQ/Clairacte-Releases/releases/download/v0.6.1-mac-preview/verification-0.6.1.json).
- [Older Windows release notes and checksum manifest](https://github.com/B3ANQ/Clairacte-Releases/releases/tag/v0.5.1-windows-legacy).
- Detailed product/developer guides are linked from the private source README and require authorized access.

## Troubleshooting

| Problem | What to check |
| --- | --- |
| Unsure where to put audio | Import it from its existing location through **Observations & audio → Importer un audio**; no watched folder is required |
| Transcription stops or fails | Keep the original, check the selected model, available space and local engine status, then use **Reprendre les parties restantes** |
| Writing assistant unavailable | Start local Ollama, verify the compatible model is installed and refresh availability in **Paramètres** |
| Saving fails | Leave the document open, check free space/permissions and retry; avoid force-quitting with unsaved work |
| Update check reports no service/feed | The current preview has no complete stable feed yet; check the public release page manually |
| Installer fails to open in 0.6.1 | The app retains the verified download and permits retry; a changed cached file must be downloaded again |
| OS blocks installation | Check the release's signing status and official OS guidance; current builds are not publisher-verified distributions |

## Contributing and support

Source contributions are restricted to authorized collaborators in the private development repository. Coordinate proposed changes with the maintainer, preserve the immutable professional foundation, use fictitious fixtures and run `npm run verify:local`. Export-layout changes also require rendered-page review. Include the behavior changed, checks performed and remaining platform limits in a pull request; never commit credentials or professional matter data.

For a reproducible bug report, include the application version, OS/architecture, steps, expected/actual behavior and a fictitious example. Use your existing private maintainer contact or the source repository's reporting facilities when you have access. Never publish confidential matter contents, recordings, passwords or plaintext backups. Follow [SECURITY.md](https://github.com/B3ANQ/Transcriptor/blob/main/SECURITY.md) for private vulnerability reporting.

## Creator and licensing

**Project creator and maintainer: [BeanQ (@B3ANQ)](https://github.com/B3ANQ).**

There is currently **no project-wide license file**. Contact the maintainer for project licensing and redistribution terms. Free local processing and public installer downloads do not constitute an open-source license declaration.

Clairacte incorporates work from [Electron](https://www.electronjs.org/), [whisper.cpp](https://github.com/ggml-org/whisper.cpp), [FFmpeg](https://ffmpeg.org/), [docx](https://github.com/dolanmiu/docx) and [Zod](https://zod.dev/), with optional [Ollama](https://ollama.com/) assistance. Bundled third-party source/license notices accompany the relevant components; the supplied fonts retain their SIL Open Font License notices. Selected external models have their own terms. The public installer repository contains distribution files and guidance; it does not publish the private development checkout.
