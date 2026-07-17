---
title: "TurboCode"
layout: project
date: 2026-07-13
image: /assets/images/turbocode-home.png
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
description: A small open-source macOS workbench for experimenting with coding agents on Swift projects.
---

<span id="top"></span>
<section class="product-hero">
    <div class="product-hero__copy">
        <span class="product-logo product-logo--hero" aria-hidden="true">
            <img src="/assets/images/turbocode-logo-provisional.png" alt="">
        </span>
        <p class="product-eyebrow">Personal open-source project</p>
        <h1>A native place to try coding agents on Swift projects.</h1>
        <p class="product-hero__lead">
            TurboCode is a small macOS app I am building to explore how different language models can read, change, build, test, and manage Git-backed Swift projects without leaving a native workspace.
        </p>
        <div class="product-actions">
            <a class="product-button product-button--primary" href="#capabilities">See what works</a>
            <a class="product-button" href="#status">Development status</a>
        </div>
        <div class="product-facts" aria-label="Project highlights">
            <span>Native SwiftUI</span>
            <span>MIT open source</span>
            <span>macOS 27</span>
            <span>Work in progress</span>
        </div>
    </div>

    <figure class="product-hero__visual">
        <img src="/assets/images/turbocode-home.png" alt="TurboCode new-chat screen with a Swift task composer and a local workspace selected">
        <figcaption>The current starting point: choose a workspace, a model profile, and describe a Swift task.</figcaption>
    </figure>
</section>

<section class="product-statement">
    <div class="product-statement__label">Why it exists</div>
    <div>
        <p class="product-eyebrow">An experiment around my own workflow</p>
        <h2>Useful tools, visible steps, modest ambitions.</h2>
        <p>TurboCode is not meant to replace Xcode or pretend that a model can run a software project on its own. It is a way to test a narrower idea: give a model well-bounded tools for Swift, keep its actions inspectable, and make it easy to review or undo the result.</p>
    </div>
</section>

<section class="product-feature" id="capabilities">
    <div class="product-feature__copy">
        <p class="product-index">01 / Workspace</p>
        <h2>Keep the conversation close to the repository.</h2>
        <p>The app can inspect the active workspace, show file results inline, and expose ordinary Git operations without turning them into invisible background work.</p>
        <ul class="product-list">
            <li>Workspace-bound file access</li>
            <li>Branches, staging, and commits</li>
            <li>Conversation history per project</li>
        </ul>
    </div>
    <figure class="product-feature__visual">
        <img src="/assets/images/turbocode-commit.png" alt="TurboCode conversation showing a Swift package tree and a completed initial Git commit">
        <figcaption>A commit appears in the conversation with its branch, hash, and line summary.</figcaption>
    </figure>
</section>

<section class="product-feature product-feature--reverse">
    <div class="product-feature__copy">
        <p class="product-index">02 / Context</p>
        <h2>Let the model consult the app’s own guide.</h2>
        <p>A bundled, versioned guide explains TurboCode’s tools and constraints to the active model. This is still experimental, but it makes product questions and tool use less dependent on a long system prompt.</p>
        <ul class="product-list">
            <li>Versioned local documentation</li>
            <li>Focused project maps</li>
            <li>Context kept close to the task</li>
        </ul>
    </div>
    <figure class="product-feature__visual">
        <img src="/assets/images/turbocode-guide.png" alt="TurboCode answering a question using its bundled product guide">
        <figcaption>The guide is presented as a visible source instead of hidden context.</figcaption>
    </figure>
</section>

<section class="product-feature">
    <div class="product-feature__copy">
        <p class="product-index">03 / Changes</p>
        <h2>Make edits reviewable and reversible.</h2>
        <p>File changes are tied to a known revision and remain visible in the conversation. The review opens the real working tree; Undo is available while that revision is still current.</p>
        <ul class="product-list">
            <li>Addition and deletion counts</li>
            <li>Review against the working tree</li>
            <li>Revision-aware Undo</li>
        </ul>
    </div>
    <figure class="product-feature__visual">
        <img src="/assets/images/turbocode-edit-review.png" alt="TurboCode showing a created README file with addition count, Review, and Undo controls">
        <figcaption>A file edit stays explicit before the next prompt or commit.</figcaption>
    </figure>
</section>

<section class="product-feature product-feature--reverse">
    <div class="product-feature__copy">
        <p class="product-index">04 / Profiles</p>
        <h2>Give smaller models a smaller job.</h2>
        <p>Built-in and custom profiles define which tools and Skills a model receives. The aim is practical rather than magical: a compact local model may work better with a short, explicit capability list.</p>
        <ul class="product-list">
            <li>Built-in and custom profiles</li>
            <li>Explicit tool selection</li>
            <li>Reusable local Skills</li>
        </ul>
    </div>
    <figure class="product-feature__visual">
        <img src="/assets/images/turbocode-custom-profiles-latest.png" alt="TurboCode Custom Profiles editor assigning selected tools and Skills to a local Llama model">
        <figcaption>A custom profile includes only the capabilities selected for that model.</figcaption>
    </figure>
</section>

<section class="product-feature">
    <div class="product-feature__copy">
        <p class="product-index">05 / Inspection</p>
        <h2>See the configuration before asking it to work.</h2>
        <p>The Tools view resolves model profiles, the active workspace, installed Skills, and runtime capabilities into one matrix. It is mostly a debugging surface, and intentionally so.</p>
        <ul class="product-list">
            <li>Backend availability</li>
            <li>Context requirements</li>
            <li>Capability matrix</li>
        </ul>
    </div>
    <figure class="product-feature__visual">
        <img src="/assets/images/turbocode-tools-latest.png" alt="TurboCode Tools view comparing model profiles and their runtime capabilities">
        <figcaption>The matrix shows which tools each configured profile can actually receive.</figcaption>
    </figure>
</section>

<section class="product-capabilities" aria-label="Current workflow summary">
    <div>
        <span>Understand</span>
        <h3>Map the workspace</h3>
        <p>Compact Swift repository maps surface declarations, relationships, imports, and source locations without reading every file.</p>
    </div>
    <div>
        <span>Verify</span>
        <h3>Use Xcode’s build system</h3>
        <p>Focused inspection, build, and test actions return bounded compiler and test diagnostics to the conversation.</p>
    </div>
    <div>
        <span>Control</span>
        <h3>Review and recover</h3>
        <p>Edits, Git operations, and approval boundaries are kept visible so the human remains responsible for the working tree.</p>
    </div>
</section>

<section class="product-docs" id="docs">
    <div class="product-docs__intro">
        <p class="product-eyebrow">Model setup</p>
        <h2>Several backends, configured locally.</h2>
        <p>TurboCode ships with a few example profiles and keeps non-secret model configuration in <code>~/.turbocode/models.json</code>. Credentials are stored in the macOS Keychain.</p>
    </div>

    <div class="product-docs__grid">
        <article>
            <span>01 / On-device</span>
            <h3>Apple Foundation Models</h3>
            <p>Runs through Apple’s framework. It needs no external server or API key, but its smaller context calls for simpler tasks and tools.</p>
        </article>

        <article>
            <span>02 / Private Cloud</span>
            <h3>Apple PCC</h3>
            <p>Uses Apple’s Foundation Models bridge while it is running locally:</p>
            <pre><code>fm serve --port 1976</code></pre>
        </article>

        <article>
            <span>03 / Local server</span>
            <h3>OpenAI-compatible models</h3>
            <p>Connect a compatible local server, such as llama-server. The example endpoint is:</p>
            <pre><code>http://127.0.0.1:8080/v1</code></pre>
        </article>

        <article>
            <span>04 / Remote API</span>
            <h3>DeepSeek</h3>
            <p>Add the API key in <strong>Settings › Providers › DeepSeek</strong>. The secret remains in Keychain.</p>
        </article>
    </div>
</section>

<section class="product-status" id="status">
    <div class="product-status__intro">
        <p class="product-eyebrow">Development status</p>
        <h2>A working prototype, not a finished product.</h2>
        <p>TurboCode is a personal open-source project under active development. It currently targets macOS 27, Xcode 27, and Swift 6, and changes frequently as I learn which parts of this approach are actually useful.</p>
    </div>
    <div class="product-status__grid">
        <article>
            <span class="product-status__label product-status__label--ready">Working now</span>
            <ul>
                <li>Workspace and session persistence</li>
                <li>Built-in and custom model profiles</li>
                <li>Reviewable, revision-bound edits</li>
                <li>Repository maps and Git tools</li>
                <li>Xcode inspection, builds, and tests</li>
                <li>Versioned configuration and Keychain credentials</li>
            </ul>
        </article>
        <article>
            <span class="product-status__label">Still rough</span>
            <ul>
                <li>Some composer controls are incomplete</li>
                <li>Approval flows need more testing</li>
                <li>Model behavior varies considerably</li>
                <li>Setup still assumes familiarity with Swift tooling</li>
                <li>Compatibility is limited to recent development releases</li>
                <li>Documentation and clean-install testing are ongoing</li>
            </ul>
        </article>
    </div>
</section>

<section class="product-install">
    <div>
        <p class="product-eyebrow">Build from source</p>
        <h2>Just a SwiftUI app.</h2>
        <p>TurboCode is written in SwiftUI and built as an ordinary macOS app. Open <code>TurboCode.xcodeproj</code>, select the <strong>TurboCode</strong> scheme, and run it from Xcode. The source is shared under the MIT License.</p>
    </div>
    <div class="product-command" aria-label="Command-line build command">
        <span>Command-line build</span>
        <code>xcodebuild -project TurboCode.xcodeproj<br>  -scheme TurboCode -configuration Debug build</code>
    </div>
</section>
