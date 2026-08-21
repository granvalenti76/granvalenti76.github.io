---
title: "TurboCode"
layout: project
date: 2026-07-13
image: /assets/images/turbocode-readme-report.png
projects: true
star: true
featured: true
tag:
  - swift
  - swiftui
  - xcode
  - llm
  - macos
category: project
author: granvalenti
description: A native SwiftUI agent harness with workspace-scoped tools for Xcode and Swift Package Manager projects.
---

<span id="top"></span>
<div class="product-landing">
    <section class="product-landing__hero">
        <div class="product-landing__hero-copy">
            <p class="product-eyebrow">Open source · SwiftUI · macOS</p>
            <h1>A native agent harness for Xcode and SwiftPM.</h1>
            <p class="product-landing__lead">TurboCode runs coding agents in a compact SwiftUI app, with workspace-scoped tools for Xcode and Swift Package Manager projects. Tool calls, edits, review, Git state, model profiles, AGENTS and Skills remain explicit.</p>
            <div class="product-actions">
                <a class="product-button product-button--primary product-button--github" href="https://github.com/granvalenti76/TurboCode" target="_blank" rel="noopener noreferrer">
                    <svg viewBox="0 0 24 24" aria-hidden="true"><path fill="currentColor" d="M12 .7a11.5 11.5 0 0 0-3.64 22.41c.58.1.79-.25.79-.56v-2.23c-3.22.7-3.9-1.37-3.9-1.37-.53-1.34-1.29-1.7-1.29-1.7-1.05-.72.08-.7.08-.7 1.17.08 1.78 1.2 1.78 1.2 1.04 1.77 2.72 1.26 3.38.96.1-.75.4-1.26.74-1.55-2.57-.3-5.27-1.28-5.27-5.68 0-1.25.45-2.28 1.19-3.08-.12-.29-.52-1.46.11-3.04 0 0 .97-.31 3.16 1.18A10.9 10.9 0 0 1 12 6.16c.98 0 1.95.13 2.87.38 2.2-1.49 3.16-1.18 3.16-1.18.63 1.58.23 2.75.11 3.04.74.8 1.19 1.83 1.19 3.08 0 4.41-2.71 5.38-5.29 5.67.42.36.79 1.06.79 2.14v3.26c0 .31.21.67.8.56A11.5 11.5 0 0 0 12 .7Z"/></svg>
                    <span>Source on GitHub</span>
                </a>
                <a class="product-button" href="{{ '/turbocode/changelog/' | relative_url }}">Changelog</a>
            </div>
        </div>

        <dl class="product-landing__specs" aria-label="Project summary">
            <div><dt>Runtime</dt><dd>Swift / SwiftUI</dd></div>
            <div><dt>Workspaces</dt><dd>Xcode / SwiftPM</dd></div>
            <div><dt>Inference</dt><dd>Local, remote, Apple</dd></div>
            <div><dt>License</dt><dd>MIT</dd></div>
        </dl>
    </section>

    <section class="product-install" id="install" aria-labelledby="install-title">
        <div>
            <p class="product-eyebrow">Install with Homebrew</p>
            <h2 id="install-title">One command. Native app.</h2>
            <p>Install the current TurboCode cask directly from the <a href="https://github.com/granvalenti76/homebrew-tap" target="_blank" rel="noopener noreferrer">granvalenti76 tap</a>. Version 0.3.3 is an alpha build, ad-hoc signed and not notarized; macOS may ask for approval in <strong>Privacy &amp; Security</strong>. The current cask requires macOS 27 beta 5.</p>
        </div>
        <div class="product-command">
            <span>Terminal</span>
            <code>brew install --cask granvalenti76/tap/turbocode</code>
            <a href="https://github.com/granvalenti76/homebrew-tap/blob/main/Casks/turbocode.rb" target="_blank" rel="noopener noreferrer">View cask recipe ↗</a>
        </div>
    </section>

    <section class="product-demo" aria-labelledby="demo-title">
        <div class="product-section-heading">
            <div>
                <p class="product-eyebrow">Recorded session</p>
                <h2 id="demo-title">A local model working through a small Swift package.</h2>
            </div>
            <p>The session inspects the repository, reports issues, edits a test, receives an inline review comment, applies the revision, and runs the test suite.</p>
        </div>
        <figure class="product-demo__frame">
            <video controls playsinline preload="metadata" poster="/assets/images/turbocode-demo-poster.jpg" aria-label="TurboCode demo using a local Qwen model">
                <source src="/assets/video/turbocode-demo-2x.mp4" type="video/mp4">
                Your browser does not support embedded video.
            </video>
            <figcaption><code>Qwen3.6-35B-A3B-UD-IQ2_XXS.gguf</code> via <code>llama-server</code> · 132K context · Q4 KV cache · playback encoded at 2×</figcaption>
        </figure>
    </section>

    <section class="product-overview" id="overview">
        <div class="product-section-heading">
            <div>
                <p class="product-eyebrow">Overview</p>
                <h2>What TurboCode is now.</h2>
            </div>
            <p>TurboCode began as a fast, compact harness designed to make smaller local models more predictable. The project has broadened: it is now a native SwiftUI agent harness with a Codex-inspired interface and a tool surface specialized for Apple development projects.</p>
        </div>

        <div class="product-technical-list">
            <article>
                <span>01</span>
                <h3>Project-specific tools</h3>
                <p>Workspace exploration, bounded file reads, ripgrep search, controlled edits, Xcode inspection, builds, tests, review, and Git operations are implemented as explicit tools scoped to the active repository.</p>
            </article>
            <article>
                <span>02</span>
                <h3>Configurable model profiles</h3>
                <p>Each profile defines its backend, context, reasoning options, and available tools. Profiles can be read-only, Git-focused, review-focused, or configured for a particular local or remote model.</p>
            </article>
            <article>
                <span>03</span>
                <h3>Repository instructions</h3>
                <p>TurboCode supports <code>AGENTS.md</code> and reusable Skills. Skills add task-specific instructions; profiles remain the authority that enables runtime capabilities.</p>
            </article>
            <article>
                <span>04</span>
                <h3>Reviewable state</h3>
                <p>Edits remain visible in the conversation and open as line-level diffs. Review comments, revision-aware undo, structured tool output, and explicit Git state keep the model’s work inspectable.</p>
            </article>
        </div>

        <aside class="product-design-note">
            <p class="product-eyebrow">Design direction / 0.3.2</p>
            <h3>Deterministic boundaries, less prescriptive reasoning.</h3>
            <p>Earlier versions tried to make the agent loop more deterministic, including the insertion of tool calls to reinforce a predefined path in specific scenarios. Work on 0.3.2 showed that too much control can also suppress useful model behavior and limit what a capable model can do.</p>
            <p>The current direction keeps capabilities, workspace access, and side effects explicit, while giving the model more freedom to decide which tool to use next. The harness still defines the boundaries; it no longer tries to prescribe every step inside them.</p>
        </aside>
    </section>

    <section class="product-models" id="models">
        <div class="product-section-heading">
            <div>
                <p class="product-eyebrow">Model backends</p>
                <h2>Use the backend that fits the task.</h2>
            </div>
            <p>TurboCode does not assume that every model should receive the same tools or the same amount of context.</p>
        </div>

        <div class="product-model-list">
            <article>
                <h3>Local models</h3>
                <p>Sufficiently capable local models can handle complete sessions. A tested configuration uses <code>Qwen3.6-35B-A3B-UD-IQ2_XXS.gguf</code> through <code>llama-server</code>, with a 132K context window and Q4 KV cache, on small and medium-sized projects.</p>
            </article>
            <article>
                <h3>Codex and DeepSeek Flash</h3>
                <p>Optional integrations provide a stronger backend when the workspace or task exceeds the practical limits of the selected local model.</p>
            </article>
            <article>
                <h3>Apple on-device and PCC</h3>
                <p>Apple Foundation Models and Private Cloud Compute can handle small, bounded tasks or participate as subagents in experimental orchestration workflows.</p>
            </article>
        </div>
    </section>

    <section class="product-tooling" id="capabilities">
        <div class="product-section-heading">
            <div>
                <p class="product-eyebrow">Current surface</p>
                <h2>Capabilities remain explicit.</h2>
            </div>
        </div>
        <dl class="product-tooling__list">
            <div><dt>Workspace</dt><dd>List files, search with ripgrep, read bounded line ranges, inspect project structure.</dd></div>
            <div><dt>Code</dt><dd>Apply controlled edits, review diffs, attach inline comments, undo against known revisions.</dd></div>
            <div><dt>Xcode</dt><dd>Inspect Xcode and SwiftPM projects, build targets, run tests, return bounded diagnostics.</dd></div>
            <div><dt>Git</dt><dd>Status, diff, branches, staging, commits, merges, rebases, pulls, and pushes as visible tool calls.</dd></div>
            <div><dt>Context</dt><dd>Model profiles, AGENTS files, Skills, cached repository maps, and backend-specific history policies.</dd></div>
        </dl>
    </section>

    <section class="product-project-status" id="status">
        <div class="product-section-heading">
            <div>
                <p class="product-eyebrow">Status</p>
                <h2>Useful today, still experimental.</h2>
            </div>
            <p>TurboCode is developed in public and changes frequently. It currently targets recent macOS, Xcode, and Swift development releases.</p>
        </div>
        <div class="product-status-columns">
            <div>
                <h3>Working</h3>
                <ul>
                    <li>Persistent workspaces and conversations</li>
                    <li>Local and remote model profiles</li>
                    <li>Workspace-scoped code and Git tools</li>
                    <li>Integrated review and inline comments</li>
                    <li>AGENTS and Skills support</li>
                </ul>
            </div>
            <div>
                <h3>Constraints</h3>
                <ul>
                    <li>Local model quality still matters</li>
                    <li>Best tested on small and medium projects</li>
                    <li>Setup assumes familiarity with Apple tooling</li>
                    <li>Approval and orchestration flows are evolving</li>
                    <li>Clean-install testing remains ongoing</li>
                </ul>
            </div>
        </div>
    </section>

    <section class="product-release-row">
        <div>
            <p class="product-eyebrow">Current release</p>
            <h2>0.3.3</h2>
            <p>Live Llama reasoning, manual context compaction, runtime details, and optional Safari browsing through MCP.</p>
        </div>
        <a href="{{ '/turbocode/changelog/' | relative_url }}">Read release notes →</a>
    </section>

    <section class="product-build">
        <div>
            <p class="product-eyebrow">Build from source</p>
            <h2>An ordinary SwiftUI app.</h2>
            <p>Clone <a href="https://github.com/granvalenti76/TurboCode">granvalenti76/TurboCode</a>, open <code>TurboCode.xcodeproj</code>, select the <strong>TurboCode</strong> scheme, and run it from Xcode. The source is available under the MIT License.</p>
        </div>
        <pre><code>xcodebuild -project TurboCode.xcodeproj \
  -scheme TurboCode \
  -configuration Debug build</code></pre>
    </section>
</div>
