---
title: "TurboCode 0.4: a more open environment"
layout: project
project_news: true
permalink: /turbocode/news/
description: An introduction to TurboCode 0.4, covering the runtime, TypeScript plugins, transcript export, and Editorial Desk.
---

<span id="top"></span>
<div class="product-news-page">
    <header class="product-news-hero">
        <div class="product-news-hero__copy">
            <p class="product-eyebrow">News / Version 0.4</p>
            <h1>A more open environment.</h1>
            <p class="product-news-hero__lead">Version 0.4 is more than a list of new features. It is the point where TurboCode starts to become an extensible environment, with clearer boundaries and tools that can take on a shape of their own.</p>
            <div class="product-news-hero__meta">
                <span>Preview presentation</span>
                <span>27 August 2026</span>
            </div>
        </div>
        <figure class="product-news-hero__image">
            <img src="{{ '/assets/images/turbocode-0-4-editorial-desk.png' | relative_url }}" alt="TurboCode Editorial Desk with a draft, a source, and editorial notes">
            <figcaption>Editorial Desk, a new native surface for working on a document and its sources.</figcaption>
        </figure>
    </header>

    <section class="product-news-section product-news-section--intro">
        <div class="product-news-section__label">
            <p class="product-eyebrow">A change in direction</p>
        </div>
        <div class="product-news-copy">
            <p>Version 0.4 is a leap forward from the previous releases. Not only because it includes more features, but because it changes, in part, how TurboCode is organized and what it can become.</p>
            <p>The work started with a runtime overhaul. From there came a TypeScript plugin system, an SDK for building your own tools, and, more recently, Editorial Desk. These are different features, but they share a common idea: TurboCode should not be a closed application with a fixed set of possibilities decided in advance.</p>
            <div class="product-news-callout">
                <p>The model can have more freedom to find its way, while important boundaries remain the responsibility of the application and the user.</p>
            </div>
        </div>
    </section>

    <section class="product-news-section">
        <div class="product-news-section__label">
            <p class="product-eyebrow">01 / Runtime</p>
            <h2>The part you do not see very often.</h2>
        </div>
        <div class="product-news-copy">
            <p>The most substantial part of 0.4 is not the part visible in the screenshots. The lifecycle of conversations, model sessions, tools, approvals, and cancellation now runs behind a shared runtime boundary.</p>
            <p>This work is primarily infrastructural. It does not add a spectacular new item to the interface, but it removes a series of hard-to-control behaviors: late results ending up in the wrong conversation, sessions remaining busy, state being duplicated between the view and the model, and differences between backends.</p>
            <p>In some cases TurboCode tried to guide the model through lists of allowed commands, path limits, and very detailed instructions. The intention was to make behavior more predictable, but the result could leave the model trapped in an artificial path.</p>
            <p>Version 0.4 gives the model more freedom. When an operation goes beyond the active workspace, however, control is not left to the model's instructions: the application shows the operation and asks the user for approval.</p>
        </div>
    </section>

    <section class="product-news-section">
        <div class="product-news-section__label">
            <p class="product-eyebrow">02 / TypeScript plugins</p>
            <h2>Tools that can have a shape of their own.</h2>
        </div>
        <div class="product-news-copy">
            <p>The most visible new feature is the TypeScript plugin system. A plugin is a regular Node project with a manifest, one or more tools, and, when needed, custom widgets.</p>
            <p>The new <code>@granvalenti/turbocode-sdk</code> defines the contract between a plugin and TurboCode. A plugin can receive the session context, be cancelled, declare its tools, and return structured results. TurboCode handles the process, execution timing, cancellation, loading, and error recovery.</p>
            <p>Plugins are discovered in the local directory, can be enabled in profiles, and can be reloaded with <code>/reload</code> without throwing away the current conversation.</p>
        </div>
        <figure class="product-news-figure product-news-figure--wide">
            <img src="{{ '/assets/images/turbocode-0-4-session-handoff.png' | relative_url }}" alt="TypeScript plugin Session Handoff displayed in a TurboCode conversation">
            <figcaption><code>Session Handoff</code> shows a structured widget produced by a plugin and inserted into the normal session flow.</figcaption>
        </figure>
    </section>

    <section class="product-news-section">
        <div class="product-news-section__label">
            <p class="product-eyebrow">03 / Transcript export</p>
            <h2>Take the conversation with you.</h2>
        </div>
        <div class="product-news-copy">
            <p>Conversations should remain useful outside TurboCode too. The transcript export menu makes it possible to take the current session wherever the next step happens.</p>
            <p>A transcript can be exported as a JSON file, sent to Apple Notes, or copied and saved as a file for use elsewhere. The JSON option preserves a structured version of the conversation, while Notes and file export make it easy to keep a readable record, share it, or continue working on it in another tool.</p>
        </div>
        <figure class="product-news-figure product-news-figure--wide">
            <img src="{{ '/assets/images/turbocode-0-4-transcript-export.png' | relative_url }}" alt="TurboCode transcript export menu with Notes and Save JSON File options">
            <figcaption>The transcript menu provides quick routes to Apple Notes, a JSON file, or a copy of the conversation.</figcaption>
        </figure>
    </section>

    <section class="product-news-section product-news-section--feature">
        <div class="product-news-section__label">
            <p class="product-eyebrow">04 / Detached widgets</p>
            <h2>A plugin can also leave the chat.</h2>
        </div>
        <div class="product-news-copy">
            <p>A widget can be detached from the conversation and opened in a separate window. At that point it is no longer just another way to display a tool's result: it becomes a small interface with a purpose of its own.</p>
            <p><em>Draft Doctor</em> is an example plugin I built. It analyzes a draft, shows a few metrics, and organizes editorial findings in its own window. The value of the example is not its name or the score it displays, but the fact that the window was built by the plugin.</p>
        </div>
        <figure class="product-news-figure product-news-figure--wide">
            <img src="{{ '/assets/images/turbocode-0-4-draft-doctor.png' | relative_url }}" alt="The Draft Doctor plugin opened in a separate window">
            <figcaption><em>Draft Doctor</em> is an example of a personal plugin with a detached surface and its own editorial interface.</figcaption>
        </figure>
    </section>

    <section class="product-news-section">
        <div class="product-news-section__label">
            <p class="product-eyebrow">05 / Editorial Desk</p>
            <h2>A native surface for writing and checking.</h2>
        </div>
        <div class="product-news-copy">
            <p>Editorial Desk is a native TurboCode feature, not a TypeScript plugin. It is separate from the main conversation and designed for working on a draft.</p>
            <p>You can start by writing directly, pasting text, or importing notes, transcripts, and files as sources. Sources remain separate from the document and can be used as reference material. The model can fact-check, check citations, make the text more neutral, tighten the opening, or prepare a summary.</p>
            <p>A revision is never applied without leaving a trace. Findings remain visible, the draft can be edited or rolled back, and the document is published to the workspace only when the user decides.</p>
        </div>
    </section>

    <section class="product-news-closing">
        <p class="product-eyebrow">A version still under construction</p>
        <h2>It is not a finished product.</h2>
        <p>Version 0.4 matters because it takes TurboCode in a broader direction, but it is not a declaration of a finished product. The runtime has been reorganized so it can grow, plugins are usable but still young, and Editorial Desk is a first experiment in a kind of work beyond programming.</p>
        <p>For me, this release mainly marks the transition from an application with a predefined path to an environment where different tools can emerge, while operations, approvals, and responsibilities remain visible.</p>
        <div class="product-actions">
            <a class="product-button product-button--primary" href="https://github.com/granvalenti76/TurboCode" target="_blank" rel="noopener noreferrer">Source on GitHub</a>
            <a class="product-button" href="{{ '/turbocode/changelog/' | relative_url }}">Technical changelog</a>
        </div>
    </section>
</div>
