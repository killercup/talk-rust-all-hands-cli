---
title: "Writing CLIs in Rust is awesome"
subtitle: "…and it's getting even better"
author: Pascal Hertleif
date: 2018-03-28
categories:
- rust
- presentation
theme: white
progress: true
slideNumber: true
history: true
---
## Hi, I'm Pascal

{[twitter],[github]}.com/killercup

[twitter]: https://twitter.com/killercup
[github]: https://github.com/killercup

::: notes

Super excited to be here at the first ever Rust All Hands!
Yesterday was surprisingly productive,
and it was super awesome to meet so many new real-life people
who I happen to already know from the Internet.

:::

# What we want to do

- - -

- famous crates: work with their authors to improve and stabilize
- write guide-level documentation
	- pitching Rust as a great lang for CLIs on the new website
	- for specific crates and use cases

# Survey

- - -

- 1,045 replies
- we'll post pretty pictures soon

- - -

![](./assets/gaps.svg)

# Areas we are focussing on

## Handling CLI input should be concise

- clap 3.0 with custom derive
- config files, env vars, CLI flags build a configuration
	- best-practice-as-a-crate

## Outputting stuff in CLI should be frictionless

- streaming and pipe handling
- logging
	- for humans and machines
	- best-practice-as-a-crate

## Testing

- assert_cli refactoring & 1.0
- guide on testing cli apps

## Distributing

- Coordinate and consolidate already existing efforts
- we can't do everything, but we can provide guidelines and scaffolding!

# This is happening fast

## Quicli

- re-exports commonly used items from other crates, e.g. structopt's derive
- provides helpers like read_file (`-> String`)
- gives you a `main!` so you can do `?` "in main" (and get logging set up)

- - -

- since quicli 0.1 in january:
	- rayon 1.0 shipped
	- failure 1.0 announced
	- CLI WG started
- quicli might become obsolete soon!
	- clap 3 with include a custom derive (ETA: Before Rust 2018)
	- `std::fs::read_string` (bikeshed half painted)
	- `?` in main will be stable _very soon_

- - -

…please keep doing this, folks

# Thanks!

## Come to the CLI WG meeting at 10pm in the "Snow" room

Slides available at [git.io/rust-all-hands-cli-wg](https://git.io/rust-all-hands-cli-wg)
