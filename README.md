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
However, *Legacy* services are still be used as they are still functional. The idea is we treat legacy service as an env or a teach,
so we can build an agent by acting with legacy service with the goal of passing test or train student model. We can use multiple agents here.

### Agents

The first agent is tester who try to measure target service by creating enough test cases.
The second agent is developer who try to create new service to pass all test cases.

### GAN methodology to improve each other

Developer try to create new service that pass as many as test cases while tester try to create new test cases to identify it from target service.

### Avoid over learning for legacy limit

Both tester and developer will be punished if any reaches to legacy limit.

## Roadmap

Below is the roadmap of planned features, with the current implementation status:

- [x] Tester agent, Understand services by testing them
  - [x] Able to figure out how to run it by looking through code+document+log
  - [x] Being able to generate tests for services
  - [ ] Summary tests as knowledge
- [ ] Developer agent, Create new service by knowledge and tests
  - [ ] Create agents by knowledge
  - [ ] Improve agents by tests
- [ ] Improve agents by feedback
  - [ ] Improve agents by reference code
  - [ ] Improve agents by feedback
