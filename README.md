# hUNC

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen.svg)
![License](https://img.shields.io/github/license/yourusername/hUNC)
![Made For](https://img.shields.io/badge/platform-Roblox-lightgrey)
![Tests](https://img.shields.io/badge/tests-6-critical)

---

## Hooked Universal Name Checker (hUNC)

**hUNC** is a lightweight, diagnostic tool for Roblox exploit environments.  
Inspired by UNC/sUNC, **hUNC** focuses not on providing an API standard, but on verifying the **integrity of the execution environment** by running a small suite of tests that validate core Lua and debug functionalities.

Rather than attempting to unify the scripting API, hUNC exists to **test the tester** — to reveal fake environments, invalid hooks, and missing metaprogramming primitives in fake or weak executors.

---

## Purpose

UNC and sUNC were fantastic tools for organizing executor APIs and catching bad actors.  
**hUNC** continues this legacy differently — by focusing on **environment authenticity**.

- No bloated features
- 6 essential tests only
- Hook/metatable detection
- Checks if you're in a native C++ executor
- Outputs clean console logs like `?/6 Functions Passed`

---

## Why?

Many executors claim to support "UNC" or "Lua fidelity", yet fake or alter key functions.  
hUNC exposes this by testing core features that real Lua environments must support.

What does this do?:

- Developers spot spoofed APIs  
- Scripters know what executors they can trust with not faking their env LOL
- Community projects like UNC evolve with better detection

---

## Features

- [x] Hook detection via `debug.getinfo`
- [x] Environment checks (`hookmetamethod`, `hookfunction`, `getfenv`, etc.)
- [x] Skips tests if native C++ executor is detected
- [x] Real-time console feedback
- [x] Output format: `FunctionName - [Genuine]` or `[Hooked]`

---

## Example Output

