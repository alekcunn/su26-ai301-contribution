# su26-ai301-contribution

# Contribution [321]: [Adapter: HuggingFace Inference Model Provider]

**Contribution Number:** 1

**Student:** Alex Cunningham  
**Issue:** https://github.com/orthogonalhq/nous-core/issues/321  
**Status:** Phase I (Complete)

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
