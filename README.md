# Prompt Engineering Playbook

A curated collection of practical prompt engineering techniques developed through hands-on testing and real-world AI workflow design.

## Introduction
This project documents specific prompt engineering methods designed for beginners and professionals alike. Each technique includes the original prompt, the outcome produced by the model (Claude), and a guide on when to apply the strategy in your own work.

---

## Table of Contents
1. [Be Clear and Direct](#1-be-clear-and-direct)
2. [Few-Shot (Multishot) Prompting](#2-few-shot-multishot-prompting)
3. [Role Prompting](#3-role-prompting)
4. [XML Tags for Structure](#4-xml-tags-for-structure)
5. [Chain of Thought Reasoning](#5-chain-of-thought-reasoning)
6. [Prompt Chaining](#6-prompt-chaining)

---

## 1. Be Clear and Direct
**Concept:** Providing precise instructions and constraints to eliminate guesswork and ensure the AI understands the specific boundaries of the task.

### The Prompt
```text
Hi Claude, I want you to think like a polymath and help me carving a learning path about what I am going say. I have always been curious about having an amazing general knowledge about space, world geography, ancient civilizations, modern world leaders, science discoveries, wars that shaped the world and more interesting topics like these. 

Please find the requirements of the plan:
1) Make a 7 day plan initially in which I can give 30 minutes everyday towards getting knowledge in fun and enjoying way.
2) YouTube! I love to learn and understand through visuals.
3) After every video you have to quiz me with open-ended questions.
4) YouTube videos can be animated/AI or regular videos but it has to be intriguing and damn interesting as I have teenagers energy for this.
5) Sequencing of the learning is of utmost importance.
```

* **Outcome:** Claude generated a logical 7-day curriculum using high-quality visual creators (melodysheep, Kurzgesagt, etc.), complete with specific quiz questions for each session.
* **When to use:** When you need a highly structured output that must satisfy multiple specific conditions simultaneously.

---

## 2. Few-Shot (Multishot) Prompting
**Concept:** Providing the AI with completed examples of the desired output to dictate the exact format, tone, and level of detail.

### The Prompt
```text
<role>You are a freelancing career advisor specializing in AI automation roles.</role>
<context>I have skills in Claude, Make.com, and n8n. I'm based in India, targeting remote work paid in USD/EUR/GBP.</context>

<instruction>Find 5 real freelancing opportunities. For each one, use the format shown in my example.</instruction>

<example>
Platform: Upwork
Role: AI Workflow Automation Specialist
What they need: Build automated email classification system using Claude API
Rate: $40-75/hr
Why I'm a fit: My Claude + Make.com skills directly match this requirement
How to apply: Highlight my prompt engineering portfolio and demo videos
</example>
```

* **Outcome:** The model mirrored the 6-field structure perfectly for all 5 suggestions, ensuring data consistency.
* **When to use:** When you need a specific, repeatable output format for data extraction or reporting.

---

## 3. Role Prompting
**Concept:** Assigning a professional persona to the AI to anchor its responses in a specific domain of expertise.

### The Prompt
```text
You are a career coach specializing in AI careers. Review LinkedIn headlines using this format:

Example:
1. Headline: AI automation specialist
Strength: I build AI automations that save teams 10+ hours/week | Claude & Make.com specialist.
Weakness: [over enthusiastic at times]
```

* **Outcome:** Claude adopted a critical, professional tone, identifying that "Specialist" labels were too passive and suggesting higher-value "Consultant" alternatives.
* **When to use:** When you need a specific professional perspective or specialized analytical voice.

---

## 4. XML Tags for Structure
**Concept:** Using tags like `<role>` or `<context>` to separate instructions from background data, preventing the AI from getting confused by "noisy" prompts.

### Implementation
* `<role>`: Sets the persona.
* `<context>`: Provides background details.
* `<instruction>`: Defines the core task.
* `<example>`: Shows the desired output.

* **Outcome:** Highly organized prompts led to significantly higher accuracy, as the model could distinguish between what it *is* and what it *does*.
* **When to use:** For complex, multi-part prompts where data and instructions might otherwise blend together.

---

## 5. Chain of Thought Reasoning
**Concept:** Forcing the AI to display its internal reasoning process before reaching a final conclusion.

### The Prompt
```text
<instruction>
If you had to choose one freelancing opportunity for me, which one would it be? 
Think step by step before giving me your verdict.
</instruction>
```

* **Outcome:** The AI generated a 4-step logical breakdown—assessing skill match, difficulty, and ROI—before providing the final recommendation.
* **When to use:** For complex decision-making, logic problems, or when you need to verify the "why" behind an AI's answer.

---

## 6. Prompt Chaining
**Concept:** Breaking a large task into a sequence of smaller, interconnected prompts where the output of one becomes the input for the next.

### Workflow Example
1.  **Prompt 1 (Extract):** Converts raw email text into a structured JSON object.
2.  **Prompt 2 (Classify):** Analyzes the JSON to determine category and urgency.
3.  **Prompt 3 (Respond):** Drafts a professional response based on the classification and urgency.

* **Outcome:** A highly reliable automation flow where each step focused on a single objective, reducing errors found in "all-in-one" prompts.
* **When to use:** For building robust AI agents or automated workflows in tools like Make.com or n8n.

---

## About the Author
**Azhar Shaikh** *Claude Certified | AI Automation & Workflow Architect*

* **Certifications:** AI Fluency (Anthropic) & Claude 101 (Anthropic)
* **Focus:** AI Automation, Prompt Engineering, and Workflow Design.
* **Tools:** Claude, Make.com, n8n.
