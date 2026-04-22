# Prompt Engineering Playbook

## Introduction

This project is a curated collection of prompt engineering techniques that I have learned, practiced, and tested through hands-on work. It is designed for beginners, learners, and professionals who want to understand how to write better prompts and build practical AI workflows.

## What's Inside

This repository will document the following prompt engineering techniques:

- Be Clear and Direct  
- Few-Shot (Multishot) Prompting  
- Role Prompting (System Prompts)  
- XML Tags for Structure  
- Chain of Thought Reasoning  
- Prompt Chaining (Multi-Step Workflows)

## Technique 1: Be Clear and Direct

**What it is:**  
Be clear and direct means giving precise, unambiguous instructions so the AI knows exactly what is expected.

**My prompt:**  
```
Create a 30-minute daily learning plan for me. Use only YouTube videos. After each video, include a short quiz. Keep the plan flexible but detailed.
```

**What happened:**  
Claude produced a daily learning schedule with clear steps: each day included a specific YouTube video, a quiz, and a total time breakdown. The specificity helped focus the AI.

**When to use this:**  
Use this when you need a structured, time-bound learning plan that stays on track.

---

## Technique 2: Few-Shot (Multishot) Prompting

**What it is:**  
Few-shot prompting means providing the AI with examples of what you want, so it can mirror the format and style.

**My prompt:**  
```
I want you to list freelancing opportunities for AI specialists. Use these examples:  
1. Data Annotation Specialist – creating labeled datasets for machine learning.  
2. AI Prompt Engineer – crafting prompts to optimize AI responses.  
List at least three more in the same format.
```

**What happened:**  
Claude gave me a structured list of freelancing roles, following the exact format I provided. Each example matched the style I set, making the results precise.

**When to use this:**  
Use this when you want the AI to follow a certain structure or format based on examples you give.

---


## About the Author

Azhar Shaikh  
Claude Certified, currently building AI automation solutions and practical AI workflows.

## Tools Used

- Claude by Anthropic
