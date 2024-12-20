# services-to-agents

## Table of Contents

- [Overview](#overview)
- [Roadmap](#roadmap)

## Overview

This tool is to convert *legacy* services especially with REST API interface to multi-agents.

### Initial

*Legacy* services is hard to maintain because:

- It only works with special(version) dependency libraries/services/env that's not available for everyone.
- It's hard to extend current code for new feature without lots of refactoring due to tech debt.
- Few people even nobody understand code due to limited/no document.
However, *Legacy* services are still be used as they are still functional.

The idea here is we treat legacy service as an target, so we can use multiple agents to measure it by writing tests then minic it by passing test.

### Agents

The first agent is tester who try to measure target service by creating enough test cases.
The second agent is developer who try to create new service to pass all test cases.

### GAN methodology to improve each other

Developer try to create new service that pass as many as test cases while tester try to create new test cases to identify it from target service.

### Avoid over learning for legacy limit

Both tester and developer will be punished if any reaches to legacy limit.

## Usage

### System design

Revised version OpenHands + Claude Sonnet 3.5 is used. Session memory is persist in file.

### Deployment guidelines

Set Claude Sonnet API key with env variant LLM_API_KEY.
To run Tester, run `sh tester.sh`.
To run Developer, run `sh developer.sh`.

## Roadmap

Below is the roadmap of planned features, with the current implementation status:

- [x] Tester agent, Understand services by testing them
  - [x] Able to figure out how to run it by looking through code+document+log
  - [] Save session memory in vector DB.
- [x] Developer agent, Create new service by knowledge and tests
  - [x] Create new service by tests code
  - [ ] Improve agents to pass tests
- [ ] Improve agents by feedback
  - [ ] Improve agents by feedback
