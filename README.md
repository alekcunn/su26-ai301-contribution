# su26-ai301-contribution

# Contribution [321]: [Adapter: HuggingFace Inference Model Provider]

**Contribution Number:** 3

**Student:** Alex Cunningham  
**Issue:** https://github.com/orthogonalhq/nous-core/issues/321  
**Status:** Phase I (Incomplete)

---

## Why I Chose This Issue

This seems like a good issue because of the projects age. The project appears new and in need of some helpers. It would be rewarding if my contribution helped bring this repo off the ground into a more known AI tool.

---

## Understanding the Issue

### Problem Description

The repo is missing adapters for different AI model providers. This issue has to do with integrating with huggingface the most known AI model repository

### Expected Behavior

The software should be able to send api calls to the huggingface TGI api

### Current Behavior

The user needs to set up an openai provider which is misleading since the api is huggingface

### Affected Components

This has to do with one of the providers for the "subcortex."

---
## Reproduction Process

### Environment Setup

The struggles I faced with the set up was mostly just installing pnpm. I wanted to use npm or bun but pnpm is the framework that the repo used so I needed to configure it for my environment. I also needed to update my branch to the most recent commits that the maintainer established for us.

### Steps to Reproduce

1. Build and run the app. Using the command `pnpm dev:web`  
2. load the web page "http://localhost:4317/"
3. search settings for the huggingface-inference model settings.
4. Search source code in the `self/subcortex/providers/src/providers` folder for the huggingface-interface provider
5. Neither the app or source code shows the provider is implemented

### Reproduction Evidence

- **Commit showing reproduction:** https://github.com/alekcunn/nous-core/commit/182b74f0bb74a2b8cae8d168cf794411f9c2722c
- **My findings:** The provider for the adapter has not been implemented yet so the next steps is to implement the provider based on the maintainers specifications

---
## Solution Approach
(using u.m.p.i.r.e)
Understand: The maintainer wants a model configuration to be implemented for the huggingface inference api. It is so the software is more obvious what interface the user wants the AI to use.
Match: The software already has OpenAI api chat providers that I can use for reference. I can also look at the huggingface docs for any differences that need to be settled.
Plan: I will need to set up the huggingface-inference engine in my environment and implement a similar class to the OpenAI, llama, and anthropic providers.
Implement: 
Review: I will thoroughly review my code and develop tests to make sure all requirements are met by both me and the maintainer. I will also work with the maintainer to evaluate and adjust my code and pull request.
Evaluate: I will test the functionality both manually and using automated unit tests

---
## Testing Strategy

### Unit Tests

- [ ] Test case 1: Ensure the provider is being added to the ProviderRegistry
- [ ] Test case 2: That the provider definitions match the definitions in the provider registry and the expected definitions.
- [ ] Test case 3: The provider fails and is not added if not API key is provided

### Integration Tests
<!-- 
- [ ] Integration scenario 1
- [ ] Integration scenario 2 -->


### Manual Testing

Manually running the app and verifying functionallity 

---

## Implementation Notes

### Week 3 Progress

This week I implemented the provider for huggingface-tgi. I created 3 seperate commits (provider, tests, catalog update)
The tests are currently failing and the design for the tests are going to collide when new providers are added to the shared files



### Code Changes

- **Files modified:** added [provider.ts, definitions.ts, adapter.ts, index.ts]
- **Key commits:**
  - https://github.com/orthogonalhq/nous-core/pull/412/changes/d3b77921e6fa218181fb29ccb58be31f4013fd4a
  - https://github.com/orthogonalhq/nous-core/pull/412/changes/74d90e0bcb71f83c5993089a8ee98c0e64258894
- **Approach decisions:** A similar provider was already implemented so this one was easy to just make the same decisions as the other provider but changing variables

---

## Pull Request

**PR Link (draft):** https://github.com/orthogonalhq/nous-core/pull/412

**PR Description:** This PR has a commit with the provider implemented and its definitions. One commit contains the tests that are currently failing (standup scheduled).
    And an update to the providers catalogs that tie the other providers together

**Maintainer Feedback:**
[6/23/26] NA
[6/30/26] https://github.com/orthogonalhq/nous-core/pull/412#pullrequestreview-4575709545


**Status:** Iterating

---
