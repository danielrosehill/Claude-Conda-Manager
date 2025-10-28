# Claude Conda Manager

![Claude Code](https://img.shields.io/badge/Claude%20Code-Project-8A2BE2?style=flat&logo=anthropic&logoColor=white)
[![Claude Code Projects Index](https://img.shields.io/badge/Claude%20Code-Projects%20Index-blue?style=flat&logo=github)](https://github.com/danielrosehill/Claude-Code-Repos-Index)
[![GitHub Master Index](https://img.shields.io/badge/GitHub-Master%20Index-181717?style=flat&logo=github)](https://github.com/danielrosehill/Github-Master-Index)

A dedicated Claude Code workspace for managing and optimizing Conda environments on Daniel's Ubuntu workstation.

## Purpose

This repository serves as a **Claude Code Space** - a specialized local workspace where Claude assists with systematic Conda environment management rather than traditional code development. The goal is to maintain an efficient, well-organized collection of Conda environments optimized for AI/ML workflows on AMD ROCm hardware.

## What is a Claude Code Space?

A Claude Code Space is a dedicated repository on your local machine used for specific administrative tasks and system management through Claude Code. Unlike traditional development repositories, these spaces are:

- Focused on local system administration and maintenance
- Used for organizing complex tasks that benefit from documentation and version control
- A persistent workspace where Claude can track configurations, decisions, and changes over time
- Version-controlled for accountability and rollback capabilities

## Core Responsibilities

### Environment Management
- Create and maintain baseline general-purpose environments with commonly-needed packages
- Build specialized environments for specific workflows (ML training, STT, video processing, etc.)
- Remove duplicate or broken environments
- Verify environment functionality and package compatibility

### AMD ROCm Optimization
- Navigate complex ROCm dependency chains
- Ensure PyTorch and other frameworks are properly configured for AMD GPUs
- Maintain documentation of working ROCm + package combinations

### Documentation & Best Practices
- Track environment configurations and their purposes
- Document successful package combinations and known issues
- Provide guidance on choosing between Conda, pip, UV, and other package managers
- Suggest efficient environment-switching workflows

## User Context

### Hardware
- **CPU**: Intel Core i7-12700F (12 cores, 20 threads)
- **GPU**: AMD Radeon RX 7700 XT / 7800 XT (Navi 32, gfx1101)
- **Memory**: 64 GB RAM
- **Storage**: ~4.6 TB total available

### Primary Use Cases
- AI/ML model development and fine-tuning
- Speech-to-text processing
- Video editing and generation
- Data analysis and visualization
- General automation and scripting

### Conda Setup
- **Miniconda3**: `~/miniconda3`
- **Anaconda3**: `~/anaconda3`
- Both installations available for different purposes

## Directory Structure

```
Claude-Conda-Manager/
├── README.md                 # This file
├── CLAUDE.md                 # Instructions for Claude Code
├── envs/                     # Environment documentation and configs
├── docs/                     # Additional documentation
├── templates/                # Environment templates and recipes
├── logs/                     # Operation logs and verification results
└── backups/                  # Environment export files
```

## Key Principles

1. **Minimize Complexity**: Reuse existing environments before creating new ones
2. **ROCm First**: Prioritize ROCm compatibility for GPU-accelerated workflows
3. **Document Everything**: Track what works, what doesn't, and why
4. **Test Before Deploy**: Verify environments before declaring them ready
5. **Version Control**: Keep environment configs and documentation in Git

## Typical Workflows

### Creating a Base Environment
Claude evaluates your typical workloads and creates general-purpose environments with pre-installed heavy packages (PyTorch, TensorFlow, common ML libraries).

### Specialized Environment Setup
When you need specific capabilities (e.g., LLM fine-tuning, STT model training), Claude builds targeted environments with minimal redundancy.

### Environment Audit
Periodic reviews to identify duplicate, broken, or unused environments for cleanup.

### Dependency Resolution
When ROCm or package conflicts arise, Claude investigates and documents solutions.

## Package Manager Guidance

- **Conda**: Use for ML/AI packages, complex dependencies, and ROCm-specific builds
- **pip**: Use within Conda environments for packages not available through Conda
- **UV**: Use for lightweight, quick project venvs outside of Conda
- **pipx**: Use for isolated CLI tool installations

## Getting Started

This workspace is already configured. Simply open Claude Code in this directory and request environment management tasks:

- "Audit my current Conda environments"
- "Create a general ML environment with ROCm support"
- "Check if I have any duplicate environments"
- "Set up an environment for LLM fine-tuning"
- "Document my working PyTorch + ROCm configuration"

## Version Control

This repository is version-controlled to track:
- Environment configurations over time
- Decisions about environment organization
- Working package combinations
- Known issues and solutions

Changes are pushed to GitHub for backup and historical reference.

## Related Resources

- **Conda Documentation**: https://docs.conda.io/
- **ROCm Documentation**: https://rocm.docs.amd.com/
- **PyTorch ROCm**: https://pytorch.org/get-started/locally/

---

**Repository Type**: Claude Code Space
**Primary User**: Daniel Rosehill
**Location**: `~/repos/github/Claude-Conda-Manager`
**Last Updated**: 2025-10-28