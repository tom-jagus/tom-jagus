# ⚖️ Principles

This is a high-level summary of the principles I follow when building systems, writing code, structuring projects, or solving problems. These are meant to be portable, repeatable defaults that reduce ambiguity and support long-term clarity.

For detailed rules, standards, and examples, see the `standards/` directory.

## 🔍 Naming & Structure

Good naming is about making things easier for the next person — even if that person is me, months from now.

- I try to keep things predictable: lowercase, snake_case, and readable at a glance
- I avoid clever names unless they’re actually helpful
- Every folder exists for a reason — no nesting just for the sake of it
- If I need to guess what something is or why it’s there, I probably named it wrong

## 💾 Version Control

I use version control to tell the story of what changed, why it changed, and how it got there.

- I never commit directly to `main` — every change gets its own branch, no matter how small
- I write commit messages like notes to my future self: short, focused, and in the present tense
- Pull requests help me slow down, double-check my thinking, and document things as I go
- I try to keep branches clean and scoped — one idea at a time, easy to follow later
