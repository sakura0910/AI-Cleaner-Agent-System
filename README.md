# AI Cleaner Agent System

## Overview
This project is an AI-driven multi-agent system for intelligent C drive management on Windows.

It is designed to simulate high token consumption scenarios through long-chain reasoning and agent collaboration.

## Core Problem
Traditional disk cleanup tools cannot distinguish between:
- System-critical files
- AI development caches (e.g., model weights, IDE indexes)
- Temporary or redundant files

This may lead to accidental deletion or inefficient cleanup.

## Architecture

### 1. Scanner Agent
- Scans the entire disk
- Collects file paths, sizes, and types

### 2. Analyzer Agent
- Uses LLM (MiMo/GPT-like models) to analyze file semantics
- Determines whether files are safe to delete
- Simulates high token consumption via reasoning tasks

### 3. Executor Agent
- Makes decisions based on Analyzer results
- Performs safe cleanup with user confirmation
- Supports rollback-safe operations (simulated)

## Token Usage Simulation
- ~5000 analysis requests per day
- ~2000 tokens per request
- Estimated daily usage: 10 million tokens

## Features
- Multi-agent collaboration
- Long-chain reasoning
- AI-assisted decision making
- Safe cleanup workflow

## Usage
```bash
python cleaner.py
