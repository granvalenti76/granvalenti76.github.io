---
title: "TurboCode: a character artist takes on a coding agent"
layout: post
date: 2026-07-30
image: /assets/images/turbocode-readme-report.png
headerImage: true
tag:
  - turbocode
  - swift
  - swiftui
  - open source
  - artificial intelligence
star: false
category: blog
author: granvalenti
description: Why I built and released a native macOS coding agent on GitHub after more than twenty years in character art.
---

<nav class="post-actions" aria-label="TurboCode links">
    <a class="post-action-button post-action-button--primary" href="https://github.com/granvalenti76/TurboCode" target="_blank" rel="noopener noreferrer">
        <svg viewBox="0 0 24 24" aria-hidden="true"><path fill="currentColor" d="M12 .7a11.5 11.5 0 0 0-3.64 22.41c.58.1.79-.25.79-.56v-2.23c-3.22.7-3.9-1.37-3.9-1.37-.53-1.34-1.29-1.7-1.29-1.7-1.05-.72.08-.7.08-.7 1.17.08 1.78 1.2 1.78 1.2 1.04 1.77 2.72 1.26 3.38.96.1-.75.4-1.26.74-1.55-2.57-.3-5.27-1.28-5.27-5.68 0-1.25.45-2.28 1.19-3.08-.12-.29-.52-1.46.11-3.04 0 0 .97-.31 3.16 1.18A10.9 10.9 0 0 1 12 6.16c.98 0 1.95.13 2.87.38 2.2-1.49 3.16-1.18 3.16-1.18.63 1.58.23 2.75.11 3.04.74.8 1.19 1.83 1.19 3.08 0 4.41-2.71 5.38-5.29 5.67.42.36.79 1.06.79 2.14v3.26c0 .31.21.67.8.56A11.5 11.5 0 0 0 12 .7Z"/></svg>
        <span>View on GitHub</span>
    </a>
    <a class="post-action-button" href="/turbocode/">Product overview</a>
</nav>

Yesterday I published the first release of [TurboCode](https://github.com/granvalenti76/TurboCode), version 0.1.0, on GitHub. It is a personal project I have been working on for some time: a native macOS coding agent designed for Swift projects.

The name is still provisional. The application itself is also evolving quickly: some parts are experimental, and others will certainly change. It is not a finished product, nor is it meant to be. Instead, this release marks the point at which a private experiment has become concrete enough to be shown, used, and discussed by other people.

Before talking about the application, however, I feel the need to address something that may seem a little unusual.

## An unexpected project

I began my career as a character artist when I was around twenty-five. I took courses and started working at companies of various sizes, sometimes as a 3D generalist. And, frankly, I have always felt at home in creative professions. TurboCode, at least on the surface, has nothing to do with that world.

For a long time, I thought this distance might be a problem. Publishing software among artwork can seem inconsistent, almost like a change of identity that requires an explanation or an official statement. But a personal website is not necessarily a brand, and a person is not a professional category.

This space has always collected whatever I was learning, building, or trying to understand at a particular moment. Over the years, my interests have included 3D graphics, Linux, open source, self-hosting, automation, and, more recently, Swift and agents based on language models. The path is not linear, but it is authentic.

I do not see TurboCode as an attempt to erase what I did before. It is the result of the same curiosity applied to a different material. In digital sculpting, you observe a form, break it down, experiment, make corrections, and look for a balance between control and discovery. When I design an interface or a software workflow, I find myself following a surprisingly similar process.

Code does not replace art. At this point in my life, it is simply the medium through which I feel the need to build.

## Why I started

TurboCode began with a practical question: what should a coding agent designed specifically for Swift and macOS look like, rather than one adapted from a general-purpose tool?

Almost every agent harness I have tried follows similar principles: it is written in TypeScript, relies heavily on tool calls that execute Bash commands, and is optimized primarily for frontier models. It is a powerful approach, but it often gives the model very broad access to the system and assumes a level of reasoning that smaller models do not have.

With TurboCode, I wanted to turn those principles around: a compact native binary, an execution surface clearly limited to macOS, and tool calls defined through the Foundation framework. When command-line tools are needed, I prefer to use specific wrappers rather than expose a general-purpose shell to the model.

Another goal was to build a harness that could work well with local models. This means adapting the tools and the amount of context to the model's capabilities, instead of designing everything around the most powerful ones.

I also wanted to experiment with features built around Foundation Models: dynamic profiles, conversation summaries, removing completed tool calls from the context, and switching models while keeping the same transcript.

That need led to a SwiftUI prototype, then to a series of experiments, and finally to the application I am presenting today.

![A TurboCode session showing results and visible changes](/assets/images/turbocode-readme-report.png)

## What TurboCode is

TurboCode is an open-source macOS application for working with coding agents on SwiftUI and Swift Package Manager projects. It allows different models to read the workspace, propose or apply changes, run builds and tests, and interact with Git from within a native interface.

The central idea is not to give the model unlimited freedom, but to provide it with precise tools.

TurboCode does not expose a general-purpose shell to the model. Operations are implemented in Swift and bound to the selected workspace. Builds, tests, and analysis use tools such as `xcrun`, `xcodebuild`, and `xctest`; changes remain visible in the conversation and can be opened in a line-by-line review.

Profiles also make it possible to choose which capabilities are assigned to each model. A profile can be read-only, specialized for Git operations, or configured with a specific set of tools and Skills. Not every model needs the same capabilities or the same amount of context.

The application can use local models, Apple Foundation Models, OpenAI-compatible servers, and remote providers configured by the user. Credentials are stored in the macOS Keychain.

It is not an alternative to Xcode, nor does it claim to turn a model into an autonomous developer. It is a focused environment for experimenting with a more transparent collaboration between a person, a model, and a repository.

## Building software without pretending to have a different past

I do not have an academic background in computer science, and I do not present myself as a software engineer with decades of experience. That would be both false and pointless.

I built TurboCode by learning as I worked, reading code and documentation, making many mistakes, and relying heavily on artificial intelligence tools for support. This does not remove responsibility for the decisions involved: architecture, boundaries, interface, testing, and the direction of the project still require judgment. It does, however, mean being transparent about the process.

I still have many reservations about artificial intelligence applied to artistic creation. When it is used to replace experience, research, and personal expression, it often diminishes precisely the part of making art that I value. I experience it differently in technical work: it can be an educational tool, a way to explore complex systems, and a means of overcoming some initial barriers without pretending that expertise and verification are no longer necessary.

TurboCode comes from within this distinction. It is not a project about generating images or replacing artists. It is an experiment in using language models to understand and modify software while keeping the steps and limitations visible.

## An outsider's perspective

Coming to software from another profession brings obvious gaps, but it also offers a particular perspective.

As an artist, I am used to evaluating tools not only by how many features they offer, but also by how they support the work. An interface can encourage concentration or fragment it. A powerful feature can become counterproductive if it does not communicate its state clearly. The ability to undo, compare, and understand what has changed is not a technical detail: it affects the confidence with which we experiment.

These principles guided TurboCode more than any desire to compete with established products. I wanted an application that was lightweight, consistent with macOS, and transparent enough for me to understand what was happening. It is a tool built primarily around my own needs, but I believe some of them may be shared by other developers, enthusiasts, or people who are learning.

Being an outsider does not automatically make a project better. It does, however, make me ask questions that I might have taken for granted in a more familiar environment.

## Why publish it

I could have continued using TurboCode as a private project. Publishing it instead means accepting its limitations, allowing other people to read its code, and seeing whether the ideas behind it work beyond my own computer.

The repository is available on [GitHub](https://github.com/granvalenti76/TurboCode) under the MIT License. TurboCode currently targets recent versions of macOS, Xcode, and Swift. Setting it up still requires some familiarity with Apple's development tools, and not every workflow is polished.

I therefore do not recommend trusting it with an important project without Git, backups, and a normal degree of caution. It is a working prototype, not a mature product.

The name itself may change. “TurboCode” began as a working title and remained long enough to end up in the repository, the interface, and this article. For now, it describes the project, but I do not consider it final.

## A starting point

Publishing TurboCode does not mean declaring a new professional identity, nor does it mean asking the audience who followed my artwork to suddenly become interested in programming.

It simply means honestly showing what I am focusing on today.

Some people will find this change far removed from the reasons they first followed me, and that is understandable. Others may recognize themselves in the idea that a career does not have to be a straight line, or that creativity does not belong to a single medium. For me, it is enough to let both things be true.

[TurboCode](https://github.com/granvalenti76/TurboCode) is already available on GitHub as release 0.1.0. If you work with Swift, experiment with local models, or are interested in more focused and transparent coding agents, you can try it, read the source, or simply follow its development.

It is still a provisional project, built by a person in transition and born from many questions. That is precisely why this feels like the right time to share it.
