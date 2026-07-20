---
title: "TurboCode"
layout: project
date: 2026-07-13
image: /assets/images/turbocode-readme-report.png
projects: true
star: true
tag:
  - swift
  - swiftui
  - xcode
  - llm
  - macos
category: project
author: granvalenti
description: A native open-source macOS coding agent built for Swift projects.
---

<span id="top"></span>
<section class="product-hero">
    <div class="product-hero__copy">
        <span class="product-logo product-logo--hero" aria-hidden="true">
            <img src="/assets/images/turbocode-logo-provisional.png" alt="">
        </span>
        <p class="product-eyebrow">Open-source macOS coding agent</p>
        <h1>Swift from Swift, with every step in view.</h1>
        <p class="product-hero__lead">
            TurboCode is a native macOS coding agent for SwiftUI and Swift Package Manager projects. It lets different language models read, edit, build, test, and manage Git-backed workspaces without leaving a focused SwiftUI app.
        </p>
        <div class="product-actions">
            <a class="product-button product-button--primary product-button--github" href="https://github.com/granvalenti76/TurboCode" target="_blank" rel="noopener noreferrer">
                <svg viewBox="0 0 24 24" aria-hidden="true"><path fill="currentColor" d="M12 .7a11.5 11.5 0 0 0-3.64 22.41c.58.1.79-.25.79-.56v-2.23c-3.22.7-3.9-1.37-3.9-1.37-.53-1.34-1.29-1.7-1.29-1.7-1.05-.72.08-.7.08-.7 1.17.08 1.78 1.2 1.78 1.2 1.04 1.77 2.72 1.26 3.38.96.1-.75.4-1.26.74-1.55-2.57-.3-5.27-1.28-5.27-5.68 0-1.25.45-2.28 1.19-3.08-.12-.29-.52-1.46.11-3.04 0 0 .97-.31 3.16 1.18A10.9 10.9 0 0 1 12 6.16c.98 0 1.95.13 2.87.38 2.2-1.49 3.16-1.18 3.16-1.18.63 1.58.23 2.75.11 3.04.74.8 1.19 1.83 1.19 3.08 0 4.41-2.71 5.38-5.29 5.67.42.36.79 1.06.79 2.14v3.26c0 .31.21.67.8.56A11.5 11.5 0 0 0 12 .7Z"/></svg>
                <span>View on GitHub</span>
            </a>
            <a class="product-button" href="#philosophy">Why TurboCode</a>
            <a class="product-button" href="#status">Development status</a>
        </div>
        <div class="product-facts" aria-label="Project highlights">
            <span>Under 70 MB idle</span>
            <span>Native SwiftUI</span>
            <span>No shell by design</span>
            <span>MIT open source</span>
        </div>
    </div>

    <figure class="product-hero__visual">
        <img src="/assets/images/turbocode-readme-report.png" alt="TurboCode conversation showing a completed README report with visible file changes">
        <figcaption>A structured coding session: workspace tools, edits, reasoning, review, and model selection remain in one native interface.</figcaption>
    </figure>
</section>

<section class="product-statement" id="philosophy">
    <div class="product-statement__label">Philosophy</div>
    <div>
        <p class="product-eyebrow">A precise scope, not an Xcode clone</p>
        <h2>Small footprint. Native tools. Human control.</h2>
        <p>TurboCode is designed to sit comfortably beside Xcode, simulators, and browsers: it uses less than 70 MB of memory when idle. Its scope is intentionally narrow—a macOS coding agent specialized in Swift—and its tool loop is written in Swift around <code>xcrun</code>, <code>xcodebuild</code>, and <code>xctest</code>, with no general-purpose shell exposed to the model.</p>
    </div>
</section>

<section class="product-feature" id="capabilities">
    <div class="product-feature__copy">
        <p class="product-index">01 / Structured conversation</p>
        <h2>More useful than a wall of text.</h2>
        <p>Tool results become native, contextual views. Edits show their line counts in the conversation, and Review opens a line-by-line diff captured when the change was applied. Undo remains tied to the real working-tree revision.</p>
        <ul class="product-list">
            <li>Integrated diff review</li>
            <li>Revision-aware Undo</li>
            <li>Structured tool results</li>
        </ul>
    </div>
    <figure class="product-feature__visual">
        <img src="/assets/images/turbocode-review-changes-2026.png" alt="TurboCode Review Changes sheet displaying README additions and deletions line by line">
        <figcaption>The integrated reviewer makes the exact patch inspectable without leaving the session.</figcaption>
    </figure>
</section>

<section class="product-feature product-feature--reverse">
    <div class="product-feature__copy">
        <p class="product-index">02 / Repository intelligence</p>
        <h2>Give each model the right amount of context.</h2>
        <p>TurboCode maps declarations, file relationships, imports, and source locations into a compact repository view. Map depth adapts to the selected backend: lighter for local models, richer for more capable ones, and cached for fast reuse.</p>
        <ul class="product-list">
            <li>Adaptive workspace maps</li>
            <li>Bounded file access</li>
            <li>Cached project context</li>
        </ul>
    </div>
    <figure class="product-feature__visual">
        <img src="/assets/images/turbocode-tools-2026.png" alt="TurboCode Tools view comparing model profiles and runtime capabilities">
        <figcaption>The Tools view resolves the active workspace, profiles, Skills, and runtime capabilities into one transparent matrix.</figcaption>
    </figure>
</section>

<section class="product-feature">
    <div class="product-feature__copy">
        <p class="product-index">03 / Model profiles</p>
        <h2>Specialize the agent, not just the prompt.</h2>
        <p>Built-in and custom profiles decide which tools and reusable Skills a model receives. A profile can be Git-only, read-only, or focused on review, keeping the available surface appropriate to the task and the model.</p>
        <ul class="product-list">
            <li>Explicit tool selection</li>
            <li>Reusable Skills</li>
            <li>Versioned configuration</li>
        </ul>
    </div>
    <figure class="product-feature__visual">
        <img src="/assets/images/turbocode-custom-profiles-2026.png" alt="TurboCode Custom Profiles editor assigning selected tools and Skills to a local Llama model">
        <figcaption>A custom GitHub Assistant profile receives only the capabilities selected for its job.</figcaption>
    </figure>
</section>

<section class="product-feature product-feature--reverse">
    <div class="product-feature__copy">
        <p class="product-index">04 / Visible Git</p>
        <h2>Keep repository operations in the loop.</h2>
        <p>Branching, staging, committing, merging, rebasing, pulling, and pushing are explicit tool calls—not invisible commands in the background. The active model profile and branch remain visible while the conversation continues.</p>
        <ul class="product-list">
            <li>Review before apply</li>
            <li>Branch and commit summaries</li>
            <li>Visible model switching</li>
        </ul>
    </div>
    <figure class="product-feature__visual">
        <img src="/assets/images/turbocode-model-picker-git-2026.png" alt="TurboCode conversation showing a completed Git commit and the model profile picker">
        <figcaption>Switch model or reasoning level without losing the session, while the Git result remains part of the conversation.</figcaption>
    </figure>
</section>

<section class="product-capabilities" aria-label="Design principles">
    <div>
        <span>Native</span>
        <h3>Follow the macOS HIG</h3>
        <p>SwiftUI, progressive disclosure, collapsible navigation, and familiar sheets keep workspaces, sessions, tools, and settings close without crowding the main task.</p>
    </div>
    <div>
        <span>Traceable</span>
        <h3>Use Xcode’s own tools</h3>
        <p>Project inspection, builds, tests, and compiler diagnostics run through Apple’s development tools and return bounded results to the conversation.</p>
    </div>
    <div>
        <span>Private by choice</span>
        <h3>Control where inference runs</h3>
        <p>Use Apple on-device inference, a local OpenAI-compatible server, Apple PCC, or a configured remote provider. Credentials remain in Keychain.</p>
    </div>
</section>

<section class="product-docs" id="docs">
    <div class="product-docs__intro">
        <p class="product-eyebrow">Model profiles</p>
        <h2>Local first, with room for larger backends.</h2>
        <p>Profiles can switch models without discarding the session. Non-sensitive endpoints and capabilities live in <code>~/.turbocode/models.json</code>; execution, Skill, agent, and Git policies live in <code>~/.turbocode/config.json</code>.</p>
    </div>

    <div class="product-docs__grid">
        <article>
            <span>01 / On-device</span>
            <h3>Apple Foundation Models</h3>
            <p>Runs locally through Apple’s framework with no server or API key. It can also serve as the entry point for the experimental orchestrator.</p>
        </article>

        <article>
            <span>02 / Private Cloud</span>
            <h3>Apple PCC</h3>
            <p>Uses the Foundation Models bridge while it is running locally:</p>
            <pre><code>fm serve --port 1976</code></pre>
        </article>

        <article>
            <span>03 / Local server</span>
            <h3>OpenAI-compatible models</h3>
            <p>Connect a local model server such as <code>llama-server</code>. The example endpoint is:</p>
            <pre><code>http://127.0.0.1:8080/v1</code></pre>
        </article>

        <article>
            <span>04 / Remote API</span>
            <h3>DeepSeek</h3>
            <p>Configure a remote model in Settings. Secrets are stored in the macOS Keychain rather than TurboCode’s JSON files.</p>
        </article>
    </div>
</section>

<section class="product-status" id="status">
    <div class="product-status__intro">
        <p class="product-eyebrow">Project status</p>
        <h2>A working prototype under active development.</h2>
        <p>TurboCode currently targets macOS 27, Xcode 27, and Swift 6. It is useful today, but still changes frequently as its model integrations, approval boundaries, and native workflows are tested.</p>
    </div>
    <div class="product-status__grid">
        <article>
            <span class="product-status__label product-status__label--ready">Working now</span>
            <ul>
                <li>Workspace and session persistence</li>
                <li>Built-in and custom model profiles</li>
                <li>Reviewable, revision-bound edits</li>
                <li>Adaptive repository maps and structured Git tools</li>
                <li>Xcode project inspection, builds, and tests</li>
                <li>Versioned configuration and Keychain credentials</li>
            </ul>
        </article>
        <article>
            <span class="product-status__label">Still to improve</span>
            <ul>
                <li>Some composer and secondary controls are incomplete</li>
                <li>Approval flows need broader testing</li>
                <li>Model behavior varies considerably between backends</li>
                <li>Setup assumes familiarity with Swift tooling</li>
                <li>Compatibility is limited to recent development releases</li>
                <li>Clean-install testing and documentation are ongoing</li>
            </ul>
        </article>
    </div>
</section>

<section class="product-install">
    <div>
        <p class="product-eyebrow">Build from source</p>
        <h2>An ordinary SwiftUI app.</h2>
        <p>Clone <a href="https://github.com/granvalenti76/TurboCode">granvalenti76/TurboCode</a>, open <code>TurboCode.xcodeproj</code>, select the <strong>TurboCode</strong> scheme, and run it from Xcode. The source is available under the MIT License.</p>
    </div>
    <div class="product-command" aria-label="Command-line build command">
        <span>Command-line build</span>
        <code>xcodebuild -project TurboCode.xcodeproj<br>  -scheme TurboCode -configuration Debug build</code>
    </div>
</section>
