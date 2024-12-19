# services-to-agents

## Table of Contents
- [Overview](#overview)
- [Roadmap](#roadmap)


## Overview
This tool is to convert *legacy* services especally with REST API interface to multi-agents.

## Initial
*Legacy* services is hard to maintain because:
- It's binded to special(version) dependency libraries/services/env that's either out of date or not avaiable for everyone.
- It's hard to extend current code for new feature without lots of refactoring due to tech debt.
- Few people even nobody understand code due to limited/no document.


## Roadmap
Below is the roadmap of planned features, with the current implementation status:

- [x] Understand services by testing them
  - [x] Able to figure out how to run it by looking through code+document+log
  - [x] Being able to generate tests for services
  - [ ] Summary tests as knowledges
- [ ] Create agents by knowledges and tests
  - [ ] Create agents by knowledges
  - [ ] Improve agents by tests
- [ ] Improve agents by feedback
  - [ ] Improve agents by reference code
  - [ ] Improve agents by feedback
