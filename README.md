# BreadBoard: The Proletarian Language Model WebUI

## Intro
SillyTavern is too convoluted. Mikupad is too spartan. Kobo is too legacybrained. Wyvern is too proprietary. OWUI is too delusional. LMStudio is too bloated. Ooba is too Ooba. We need a webUI that doesn't suck.

Inspired by *ComfyUI*, *DragonRuby*, and *Neovim*, BreadBoard is a hypertext-driven UI for interacting with large language models and the various peripherals involved with the same.
BreadBoard provides you everything you need and nothing you don't; and has an ergonomic interface for making extensions, based on established standards that the average nerd can learn about in a weekend.

## Goals

- Web-based, HTML+JS, HATEOAS-ish.
- Quasi-object-oriented prompt builder based on JSON and template literals.
- Support for the Tavern "character card" standard, where character cards are a JSON object whose properties can be addressed directly.
- A RESTful interface that can be understood by non-SWEs for building extensions, inspired by SillyTavern Extras. If your tool can emit JSON, you can code it in whatever language you want.
- Modular; provide scaffolding for building first-class modules in HTML and JS without a black-belt in web development
- Non-modal; No "modes": A single run should be capable of querying many types of APIs in user-definable flows, idiomatically called "circuits".

## Non-Goals

- Multi-user support. BreadBoard is not intended for production use.
- Security. BreadBoard provides no mechanism for locking down your instance or its data. Don't expose it outside of your LAN.
- MCP. While technically interesting, I don't believe that mass adoption of a protocol administered by a single company is good for the health of the scene. A module that enables MCP could be developed by a third party, but it's not something we're interested in pursuing.
- Graph interface. While the graph interface works great for ComfyUI, SillyTavern users don't want to look at spaghetti all the time. A graph-based frontend for the Circuit Builder could be possible.

## "Base" UI Modules:

- Chat (Queries Chat Completions APIs)
- Notebook (Queries Text Completions APIs)
- Circuit Builder (a GUI workbench for building prompts through integrating parts defined in the parts bin as well as "tool" modules)
- Parts Bin (a GUI frontend for defining K:V pairs which are used in the prompt builder)
- Toolbox (A stowable holding place for modules which are only interacted with sometimes)

The documentation is in sections on HackMD.

Next: [The Anatomy of a Circuit](https://hackmd.io/naFS7CblRzuKg0CvDtp06A)
