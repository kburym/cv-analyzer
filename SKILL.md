---
name: cv-analyzer
description: CV аналайзер. Checks whether a CV in a Markdown file contains a person's name and answers only true or false. Use when the user asks to check whether a CV has a name, or passes a CV .md file to cv-analyzer.
---

# CV Analyzer (CV аналайзер)

This skill does exactly one thing: it checks whether a CV contains a person's name.

## Input

A path to a Markdown (`.md`) file with a CV.

## Output

Exactly one word, nothing else: `true` or `false`.

No explanations, no extra text, no formatting, no punctuation.

## Instructions

### Step 1: Read the file
Read the `.md` file at the given path. If the file cannot be read, output `false`.

### Step 2: Look for a name
A CV has a name when the document identifies a person by a personal name, usually a first name and last name. The most common places:
- the first heading (for example `# John Doe`);
- a bold or plain line at the very top of the document.

A job title (for example `Full Stack Developer`), a company, a section heading (`Про мене`, `Досвід роботи`) or a contact detail (email, phone, link) alone is NOT a name.

### Step 3: Answer
- A person's name is present: output `true`.
- No person's name is present: output `false`.
