# Aether Architecture Overview

## High-Level Flow

1. Artist uploads audio stems / tracks + optional visual references
2. Feature extraction (audio + visual)
3. Topological + geometric analysis → personal vibe manifold
4. Constrained generation (audio and/or visual) stays near the manifold
5. Privacy layer ensures models and data remain under artist control

## Core Modules

- **core/** → Manifold construction, TDA, geometric losses, distance metrics
- **audio/** → Feature extraction + constrained generative models
- **visual/** → Visual generation conditioned on the shared manifold embedding
- **privacy/** → Local inference + future zkML path
- **api/** → Backend services and orchestration
- **web/** → Interactive dashboard (3D manifold explorer + controls)

## Design Goals
- Mathematical transparency where possible
- Local-first by default
- Strong separation between core math and generation layers
- Extensible to new modalities later
