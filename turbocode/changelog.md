---
title: "TurboCode Changelog"
layout: project
project_changelog: true
permalink: /turbocode/changelog/
description: Release notes and updates for TurboCode, a native open-source macOS coding agent for Swift.
---

<span id="top"></span>
<section class="changelog-page">
    <header class="changelog-page__header">
        <a class="changelog-page__back" href="{{ '/turbocode/' | relative_url }}">← TurboCode</a>
        <p class="product-eyebrow">Release notes</p>
        <h1>Changelog</h1>
        <p>Changes to the native macOS coding agent for Swift.</p>
    </header>

    <article class="changelog-release" id="release-0-5-0">
        <header class="changelog-release__header">
            <div>
                <h2>0.5.0</h2>
                <p>Current release · Prerelease · Released 6 September 2026</p>
            </div>
            <a href="https://github.com/granvalenti76/TurboCode/releases/tag/v0.5" target="_blank" rel="noopener noreferrer">View release on GitHub ↗</a>
        </header>

        <p class="changelog-release__summary">TurboCode 0.5 is a prerelease focused on controllable agent collaboration, profile-driven workers, and a more reviewable runtime workflow for Swift and SwiftUI development on macOS.</p>

        <div class="changelog-release__facts">
            <span>Agent collaboration</span>
            <span>Worker pools</span>
            <span>Codex profiles</span>
            <span>First-launch onboarding</span>
        </div>

        <section class="changelog-section">
            <h3>Highlights</h3>
            <ul>
                <li><strong>Runtime steering.</strong> Queue corrections while a turn is running, with explicit Codex turn and steer support for more responsive intervention.</li>
                <li><strong>Asynchronous delegation.</strong> Delegate work to worker pools and track concurrent activity without losing visibility into the overall session.</li>
                <li><strong>Explicit worker routing.</strong> Route work through <code>worker_id</code> and worker role descriptions, with busy-worker protection to avoid conflicting assignments.</li>
                <li><strong>Codex profiles.</strong> Profiles can provide worker-specific tool overrides, making the capabilities of each collaborating agent explicit.</li>
                <li><strong>Transcript projection.</strong> Transcript context projection is improved, with reversible exclusions for tool exchanges when a worker needs a more focused context.</li>
                <li><strong>Typed runtime receipts.</strong> Native and Codex runtimes now use executor-neutral streaming and typed tool receipts, giving the UI a more consistent view of progress and results.</li>
                <li><strong>Custom Profiles / Agent Team.</strong> The workspace for composing custom profiles and agent teams has been refined for collaborative workflows.</li>
                <li><strong>TypeScript onboarding.</strong> Plugin examples and SDK onboarding now cover more of the path from a first extension to a usable tool.</li>
                <li><strong>Additive first launch.</strong> TurboCode creates the local <code>~/.turbocode/</code> layout on first launch while preserving existing configuration and model endpoints during onboarding and migration.</li>
            </ul>
        </section>

        <section class="changelog-section">
            <h3>Onboarding</h3>
            <ul>
                <li><strong>Local configuration.</strong> The first-launch layout includes <code>models.json</code>, <code>config.json</code>, and <code>profiles.json</code>, along with sessions, diagnostics, built-in Skills, TypeScript plugins and SDK files, a repository-map cache, and official and user documentation.</li>
                <li><strong>Migration safety.</strong> Existing user configuration and model endpoints are preserved when the new local layout is created or migrated.</li>
            </ul>
        </section>

        <section class="changelog-section">
            <h3>Verification</h3>
            <ul>
                <li><strong>Bootstrap tests.</strong> <code>FirstLaunchBootstrapTests</code> passed 9/9 checks.</li>
                <li><strong>Repository hygiene.</strong> <code>git diff --check</code> passed, and the <code>dev</code> branch was merged from the existing 0.4 baseline.</li>
                <li><strong>Prerelease note.</strong> Real-provider interactive validation remains a release-gate task for the prerelease.</li>
            </ul>
        </section>

        <section class="changelog-section">
            <h3>Demo</h3>
            <figure class="product-demo__frame">
                <video controls playsinline preload="metadata" poster="{{ '/assets/images/turbocode-demo-poster.jpg' | relative_url }}" aria-label="TurboCode 0.5 demo">
                    <source src="{{ '/assets/video/turbocode-0-5-demo.mp4' | relative_url }}" type="video/mp4">
                    Your browser does not support embedded video.
                </video>
                <figcaption>Demo della prerelease TurboCode 0.5, allegata alla release GitHub.</figcaption>
            </figure>
        </section>
    </article>

    <article class="changelog-release" id="release-0-4-0">
        <header class="changelog-release__header">
            <div>
                <h2>0.4.0</h2>
                <p>Previous release · Released 30 August 2026</p>
            </div>
            <a href="https://github.com/granvalenti76/TurboCode/blob/main/CHANGELOG.md" target="_blank" rel="noopener noreferrer">View full changelog on GitHub ↗</a>
        </header>

        <p class="changelog-release__summary">TurboCode 0.4 turns the application into a broader native agent harness, with a shared runtime, controlled TypeScript extensions, a more direct workspace and Git workflow, and new native macOS surfaces for managing work.</p>

        <div class="changelog-release__facts">
            <span>Shared runtime</span>
            <span>TypeScript plugins</span>
            <span>Editorial Desk</span>
            <span>Transcript export</span>
        </div>

        <section class="changelog-section">
            <h3>Highlights</h3>
            <ul>
                <li><strong>Shared runtime.</strong> Native and Codex sessions now share the same lifecycle for turns, tools, approvals, cancellation, persistence, and completion.</li>
                <li><strong>Workspace safety.</strong> File operations outside the active workspace show the exact operation and wait for explicit user approval.</li>
                <li><strong>TypeScript plugins.</strong> The new <code>@granvalenti/turbocode-sdk</code> supports typed tools, custom widgets, automatic discovery, profile activation, <code>/reload</code>, timeouts, cancellation, and crash recovery.</li>
                <li><strong>Editorial Desk.</strong> Drafts can be written, reviewed with sources and editorial findings, and published to the workspace in a controlled way.</li>
                <li><strong>Transcript sharing.</strong> A transcript can be sent to Notes or saved as JSON; multiple transcripts can be exported as a ZIP.</li>
                <li><strong>More native workflows.</strong> Workspace and chat management now includes immediate deletion, compact swipe actions, automatic conversation titles, and improved toolbar and sidebar presentation.</li>
            </ul>
        </section>
    </article>

    <article class="changelog-release" id="release-0-3-3">
        <header class="changelog-release__header">
            <div>
                <h2>0.3.3</h2>
                <p>Previous release · Released 21 August 2026</p>
            </div>
            <a href="https://github.com/granvalenti76/TurboCode/releases/tag/v0.3.3" target="_blank" rel="noopener noreferrer">View release on GitHub ↗</a>
        </header>

        <p class="changelog-release__summary">This release improves the backend used by TurboCode’s Local LLM profile, especially the Llama integration. The goal is simple: a native SwiftUI harness should remain responsive and useful with capable local models, including on Macs with 16 GB of RAM. The work also puts clearer boundaries around model capabilities and optional tools, laying the groundwork for a more modular architecture in future releases without changing the current user workflow.</p>

        <div class="changelog-release__facts">
            <span>6 features</span>
            <span>2 fixes</span>
            <span>Llama-focused</span>
            <span>16 GB Macs supported</span>
        </div>

        <section class="changelog-section">
            <h3>Features</h3>
            <ul>
                <li><strong>Live reasoning and runtime details.</strong> Llama responses now show reasoning updates while the model is working and report useful runtime details such as response time, generated tokens, and context usage.</li>
                <li><strong>Manual context compaction.</strong> Local Llama sessions can reduce older transcript content when the model is running out of room. TurboCode records a visible event so the conversation remains understandable.</li>
                <li><strong>Llama context ring.</strong> The composer now shows a Llama-only context ring after a turn completes, with used and total context values available on hover. Other profiles keep their existing footer.</li>
                <li><strong>Server configuration.</strong> Llama reads its server URL from <code>models.json</code> when the session is first created, so custom hosts and ports work consistently from the start.</li>
                <li><strong>Request-scoped reasoning updates.</strong> Reasoning updates are tied to the active model request and grouped when they arrive in quick bursts. This prevents an old request from writing into a new transcript and avoids unnecessary UI work.</li>
                <li><strong>Optional Safari browsing through MCP.</strong> Web browsing is disabled by default because MCP tools can add a large amount of text to the context; a few turns can reach roughly 25k tokens. Enable it from <code>Settings &gt; Agents &gt; Experimental</code> when using a model with fast token generation, so the extra tool work does not make the interaction feel slow.</li>
            </ul>
        </section>

        <section class="changelog-section">
            <h3>Fixes</h3>
            <ul>
                <li><strong>Changes Inspector refresh.</strong> The inspector now refreshes workspace diffs when it opens, so it reflects the current repository state.</li>
                <li><strong>Window toolbar clipping.</strong> Chat text no longer shows through the macOS window toolbar or the top scroll edge. The fix keeps the existing workbench layout and sidebar alignment intact.</li>
            </ul>
        </section>
    </article>

    <article class="changelog-release" id="release-0-3-2">
        <header class="changelog-release__header">
            <div>
                <h2>0.3.2</h2>
                <p>Earlier release · 11 commits since 0.3.1</p>
            </div>
            <a href="https://github.com/granvalenti76/TurboCode" target="_blank" rel="noopener noreferrer">View source on GitHub ↗</a>
        </header>

        <p class="changelog-release__summary">A cumulative release focused on workspace exploration, bounded file access, model context, and code review.</p>

        <div class="changelog-release__facts">
            <span>10 substantial changes</span>
            <span>9 branch-specific commits</span>
            <span>49 files involved</span>
            <span>HEAD <code>59ba81b</code></span>
        </div>

        <section class="changelog-section">
            <h3>Added</h3>
            <ul>
                <li><strong>Ripgrep search.</strong> File discovery and content search with literal text, regular expressions, paths, globs, case sensitivity, hidden files, context lines, and filename-only results. Searches respect repository ignore rules, return workspace-relative paths, and never use a shell.</li>
                <li><strong>Search activity indicator.</strong> A small terminal-style timeline indicator shows what the model is searching and where, including completion feedback that respects Reduce Motion.</li>
                <li><strong>Bounded file reading.</strong> <code>read_file</code> now reads precise, resumable line ranges, reports line and token information, stops at line boundaries, and handles minified files with a single long line.</li>
                <li><strong>Inline review comments.</strong> Local comments can be created, edited, deleted, and sent with ⌘ Return. Anchors survive refresh and line movement; ambiguous anchors become stale instead of being guessed.</li>
            </ul>
        </section>

        <section class="changelog-section">
            <h3>Changed</h3>
            <ul>
                <li><strong>Profiles and Skills.</strong> Profiles are now the only authority for runtime capabilities. Selected tools are registered directly, while Skills provide task instructions without changing the available tools.</li>
                <li><strong>Workspace discovery.</strong> <code>list_workspace</code> returns directory data without prescribing a backend-specific strategy. Xcode projects and workspaces remain ordinary directory entries.</li>
                <li><strong>Markdown presentation.</strong> Typography, spacing, lists, tables, code blocks, blockquotes, and separators now use a quieter native macOS treatment. Decorative output is normalized without changing the original conversation.</li>
                <li><strong>Review Changes and Inspector.</strong> Both surfaces have improved scrolling, line-number gutters, file sections, collapsed unchanged regions, focused expansion, and clearer change counts.</li>
                <li><strong>Swift review syntax.</strong> Swift keywords, types, attributes, numbers, strings, comments, multiline strings, raw strings, and nested multiline comments receive stateful highlighting.</li>
            </ul>
        </section>

        <section class="changelog-section">
            <h3>Fixed</h3>
            <ul>
                <li><strong>Llama prompt caching.</strong> Ordered JSON keys produce a stable KV-cache prefix, tool definitions keep their order when profiles are rebuilt, and completed tool calls remain in history for the relevant Llama profiles and overrides.</li>
                <li><strong>Backend history policy.</strong> History behavior now follows the actual backend rather than an editable profile name. Apple Foundation Models and DeepSeek keep their existing policies.</li>
                <li><strong>Legacy profile migration.</strong> Ripgrep keeps the internal legacy <code>grep</code> identifier so existing saved profiles migrate automatically. The old implicit <code>file-browser</code> Skill activation has been removed.</li>
                <li><strong>Review state.</strong> Multiple inline comments are aggregated correctly, stale comments block sending until resolved, and review drafts are cleared when changing workspace or conversation.</li>
            </ul>
        </section>

        <p class="changelog-release__footer">The review workflow has been manually tested with <code>Qwen3.6-35B-A3B-UD-IQ2_XXS.gguf</code>.</p>
    </article>
</section>
