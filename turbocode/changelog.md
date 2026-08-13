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

    <article class="changelog-release" id="release-0-3-2">
        <header class="changelog-release__header">
            <div>
                <h2>0.3.2</h2>
                <p>Current release · 11 commits since 0.3.1</p>
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
