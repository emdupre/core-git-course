---
title: "Commit advice"
teaching: 5
exercises: 0
questions:
- "How, what, and when to commit?"
- "What makes a good commit message?"
objectives:
- "Understand what makes a good commit message"
- "Know which types of files not to commit"
- "Know when to commit changes"
keypoints:
- "Commit messages explain why changes were made, so make them clear and concise"
- "Follow conventions to give a history that is both useful, and easy to read"
- "Only commit files which can't be automatically recreated"
---

### How to write a good commit message

Commit messages should explain why you have made your changes. They should mean
something to others who may read them --- including your future self in 6 months
from now.
As such you should be able to understand why something happened months
or years ago.

Well written commit messages make reviewing code much easier, and more enjoyable.
They also make interacting with the log easier --- commands like `blame`, `revert`,
`rebase`, and `log`.

[Here is an excellent summary](http://chris.beams.io/posts/git-commit/) of
best-practice, following established conventions.
It's well worth a read but the key points are given below:

1. Separate the subject from body with a blank line
2. Limit the subject line to 50 characters
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line
6. Wrap the body at 72 characters
7. Use the body to explain what and why vs. how

---

### Commit anything that cannot be automatically recreated

Typically we use version control to save anything that we create manually
e.g. source code, scripts, notes, plain-text documents, LaTeX documents.
Anything that we create using a compiler or a tool e.g. object files (`.o`,
`.a`, `.class`, `.pdf`, `.dvi` etc), binaries (`exe` files), libraries (`dll`
or `jar` files) we don't save as we can recreate it from the source. Adopting
this approach also means there's no risk of the auto-generated files becoming
out of sync with the manual ones.

We can automatically ignore such files using a `.gitignore` file!
