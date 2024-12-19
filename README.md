# services-to-agents

## Table of Contents
- [Overview](#overview)
- [Roadmap](#roadmap)


## Overview
This tool is to convert *legacy* services especally with REST API interface to multi-agents.

### Initial
*Legacy* services is hard to maintain because:
- It's binded to special(version) dependency libraries/services/env that's either out of date or not avaiable for everyone.
- It's hard to extend current code for new feature without lots of refactoring due to tech debt.
- Few people even nobody understand code due to limited/no document.
However, *Legacy* services are still be used as they are still functional. The idea is we treat legacy service as an env or a teach,
so we can build an agent by acting with legacy service with the goal of passing test or train student model. We can use mulitple agents here.

### Agents
The first agent is tester who try to measure target service with test-driven methods.


## Roadmap
Below is the roadmap of planned features, with the current implementation status:

- [x] Tester, Understand services by testing them
  - [x] Able to figure out how to run it by looking through code+document+log
  - [x] Being able to generate tests for services
  - [ ] Summary tests as knowledges
- [ ] Create agents by knowledges and tests
  - [ ] Create agents by knowledges
  - [ ] Improve agents by tests
- [ ] Improve agents by feedback
  - [ ] Improve agents by reference code
  - [ ] Improve agents by feedback
