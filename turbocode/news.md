---
title: "TurboCode 0.61: smarter tool routing"
layout: project
project_news: true
permalink: /turbocode/news/
description: What's new in TurboCode 0.6 and 0.61, from Xcode ACP integration to AnchorSignal dynamic routing for local models.
---

<span id="top"></span>
<div class="product-news-page">
    <header class="product-news-hero">
        <div class="product-news-hero__copy">
            <p class="product-eyebrow">News / Versions 0.6 and 0.61</p>
            <h1>The right tools for each request.</h1>
            <p class="product-news-hero__lead">TurboCode 0.61 lets a small on-device model choose a bounded tool package for every request. It builds on 0.6, which brought Xcode integration and richer workspace review.</p>
            <div class="product-news-hero__meta">
                <span>Current release</span>
                <span>20 September 2026</span>
            </div>
        </div>
    </header>

    <section class="product-news-section product-news-section--intro">
        <div class="product-news-section__label">
            <p class="product-eyebrow">0.61 · What’s new</p>
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

    <section class="product-news-section product-news-section--intro">
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
