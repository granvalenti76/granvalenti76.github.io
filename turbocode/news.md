---
title: "TurboCode 0.65: sets itself up"
layout: turbocode
tc_page: news
toc:
  - { id: news-0-65, title: "0.65 · First-launch setup" }
  - { id: news-0-64, title: "0.64 · Studio" }
  - { id: news-0-61, title: "0.61 · Dynamic routing" }
  - { id: news-0-6, title: "0.6 · Xcode integration" }
permalink: /turbocode/news/
description: What's new in TurboCode 0.64 and 0.65, from Studio and its Artifacts library to a first-launch setup that finds your model.
---

<div class="product-news-page">
    <header class="product-news-hero">
        <div class="product-news-hero__copy">
            <div class="crumb">turbocode / news · versions 0.64 and 0.65</div>
            <h1>TurboCode now sets itself up.</h1>
            <p class="product-news-hero__lead">TurboCode 0.65 finds your model on first launch and lets you follow a long run without interrupting it. It builds on 0.64, which turned Cowork into Studio.</p>
            <div class="product-news-hero__meta">
                <span>Current release</span>
                <span>12 November 2026</span>
            </div>
        </div>
    </header>

    <section class="product-news-section product-news-section--intro" id="news-0-65">
        <div class="product-news-section__label">
            <p class="product-eyebrow">0.65 · What’s new</p>
        </div>
        <div class="product-news-copy">
            <p>On first launch, TurboCode now looks for a model server on your Mac or at an address you type for another machine: llama-server, LM Studio, Ollama, vLLM, or Jan. With llama-server it reads the context window and vision support on its own, checks tool calls in the background, and writes the configuration only when you choose <strong>Create and Start</strong>.</p>
            <figure class="product-demo__frame">
                <img src="{{ '/assets/images/turbocode/onboarding-welcome.png' | relative_url }}" loading="lazy" alt="TurboCode welcome sheet: your model, every change reviewable, Coding and Studio.">
                <figcaption>The new welcome sheet. Setup takes about a minute.</figcaption>
            </figure>
            <p>While a model works, you can ask how it is going. The question never reaches the busy model: the on-device model answers in a card above the composer, from the live reasoning and tool calls. Steering messages now reach native models between tool rounds instead of at the end of the turn, and the Transcript has a <strong>Live</strong> view that shows tool calls as they stream.</p>
            <p>Studio gets bundled skills for web pages, printable documents, and slide decks, printed to PDF with the VM’s Chromium. And the app has a calmer look: a terracotta accent, serif titles, and a choice of translucent or solid sidebar.</p>
            <div class="product-actions">
                <a class="product-button product-button--primary" href="https://github.com/granvalenti76/TurboCode/releases/tag/v0.65" target="_blank" rel="noopener noreferrer">Release v0.65</a>
                <a class="product-button" href="{{ '/turbocode/changelog/' | relative_url }}#release-0-65">Technical changelog</a>
            </div>
        </div>
    </section>

    <section class="product-news-section product-news-section--intro" id="news-0-64">
        <div class="product-news-section__label">
            <p class="product-eyebrow">0.64 · 10 November 2026</p>
        </div>
        <div class="product-news-copy">
            <p>Version 0.64 renamed Cowork to Studio and gave it a home: four cards for web pages, data, documents, and your files, plus your most recent artifacts. Everything still runs in a sandboxed Linux VM, and nothing reaches your Mac until you approve it.</p>
            <figure class="product-demo__frame">
                <img src="{{ '/assets/images/turbocode/studio-home.png' | relative_url }}" loading="lazy" alt="TurboCode Studio home with capability cards, the Prassitele connector, and the composer.">
                <figcaption>The Studio home.</figcaption>
            </figure>
            <p>The new Artifacts library collects what each session placed in <code>/out</code>, and the inspector beside the chat opens servers left running in the VM as live pages. Models with vision can look at images inside the VM, so they can check a page they just built. Connectors let one session work with another app on your Mac; Prassitele is the first.</p>
            <div class="product-actions">
                <a class="product-button" href="https://github.com/granvalenti76/TurboCode/releases/tag/v0.64" target="_blank" rel="noopener noreferrer">Release v0.64</a>
                <a class="product-button" href="{{ '/turbocode/changelog/' | relative_url }}#release-0-64">Technical changelog</a>
            </div>
        </div>
    </section>

    <section class="product-news-section product-news-section--intro" id="news-0-61">
        <div class="product-news-section__label">
            <p class="product-eyebrow">0.61 · 20 September 2026</p>
        </div>
        <div class="product-news-copy">
            <p>Version 0.61 introduces AnchorSignal dynamic routing for Apple on-device and local Llama conversations. A small semantic model matches each request to a compact tool category, such as implementation, workspace inspection, search, Git, Xcode, guidance, or conversation. The active profile’s allowlist stays the capability boundary, so routing can only narrow what a profile already permits.</p>
            <p>The composer offers <strong>Profile</strong> and <strong>Auto</strong> modes, with a brief receipt showing the selected package and tool count. To enable it, open <strong>Settings → Agents</strong> and turn on <strong>Dynamic Routing</strong>. The first time, TurboCode downloads and verifies the model; once it is ready, Auto becomes available below the input field. Routing is not offered for DeepSeek and Codex conversations.</p>
            <div class="product-actions">
                <a class="product-button product-button--primary" href="https://github.com/granvalenti76/TurboCode/releases/tag/v0.61" target="_blank" rel="noopener noreferrer">Release v0.61</a>
                <a class="product-button" href="{{ '/turbocode/changelog/' | relative_url }}#release-0-61">Technical changelog</a>
            </div>
        </div>
    </section>

    <section class="product-news-section product-news-section--intro" id="news-0-6">
        <div class="product-news-section__label">
            <p class="product-eyebrow">0.6 · 13 September 2026</p>
        </div>
        <div class="product-news-copy">
            <p>Version 0.6 added opt-in Xcode MCP integration and a bundled headless ACP helper, so TurboCode can run as an external agent in Xcode. Workspace files can be previewed in place and reviewed with line-scoped comments that re-anchor as the document changes. Profiles gained configured workers with up to four running concurrently, a built-in Codex profile, unified <code>SKILL.md</code> handling, and session metrics for context, cache hits, and tokens.</p>
            <figure class="product-demo__frame">
                <img src="{{ '/assets/images/turbocode-0-6-workspace.png' | relative_url }}" width="3064" height="1756" loading="lazy" alt="TurboCode 0.6 showing workspace files, a Markdown preview of the Xcode ACP setup guide, and context, cache hit, and session token statistics.">
                <figcaption>TurboCode 0.6: workspace previews, Xcode ACP setup, and session metrics.</figcaption>
            </figure>
            <div class="product-actions">
                <a class="product-button" href="https://github.com/granvalenti76/TurboCode/releases/tag/v0.6" target="_blank" rel="noopener noreferrer">Release v0.6</a>
                <a class="product-button" href="{{ '/turbocode/changelog/' | relative_url }}#release-0-6-0">Technical changelog</a>
            </div>
        </div>
    </section>
</div>
