# ⚖️ Principles

These are the habits, defaults, and small rules I rely on to keep my work clear, maintainable, and useful — for myself and for anyone else who might work with me or pick up what I’ve built.

They're not set in stone, but they help me move faster, make better decisions, and stay consistent across projects.

For more detailed standards and examples, check the `standards/` folder.

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

## 📦 Code & Automation

If I’ve done something more than once and it’s even a little annoying, I’ll probably script it.

- I try to automate anything that feels repetitive, fragile, or easy to forget
- I’d rather write a small script than rely on memory or manual steps
- If it might run on another machine, I make sure it’s portable and doesn’t assume too much
- I like errors to fail loud and early — better to catch problems upfront than let them hide
