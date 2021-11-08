# Table of Contents

- [Git Commit Guidelines](#git-commit-guidelines)

# Git Commit Guidelines
## This topic can be split into two areas of concern
1. The structured set/split of the code changes (i.e. what belongs to a single commit)
2. The format of the commit message and the information provided in it

## 1. Structural split of code changes into separate commits
The cardinal rule for creating good commits is to ensure there is only one "logical change" per commit. There are many reasons why this is an important rule:

- The smaller the amount of code being changed, the quicker & easier it is to review & identify potential flaws.
- If a change is found to be flawed later, it may be necessary to revert the broken commit. This is much easier to do if 
  there are not other unrelated code changes entangled with the original commit.
- When troubleshooting problems using Git's bisect capability, small well defined changes will aid in isolating exactly 
  where the code problem was introduced.
- When browsing history using Git annotate/blame, small well defined changes also aid in isolating exactly where & why a 
  piece of code came from.

### Common pitfalls to avoid
There are some commonly encountered examples of bad things to avoid
- Mixing whitespace (i.e. formatting, styling) changes with functional code changes.
- Mixing two unrelated functional changes.
- Sending large new features in a single giant commit.

## 2. How to write a good commit message
**Style.** Markup syntax, wrap margins, grammar, capitalization, punctuation.

**Content.** What kind of information should the body of the commit message (if any) contain? What should it not contain?

**Metadata.** How should issue tracking IDs, etc. be referenced?

### Seven basic rules of good commit messages:
1. Separate subject from body with a blank line
2. Limit the subject line to 50 characters
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mode in the subject line
6. Wrap the body at 72 characters
7. Use the body to explain what and why vs. how

## Here’s a model Git commit message:
```
Summarize changes in around 50 characters or less

More detailed explanatory text, if necessary. Wrap it to 72 characters.
In some contexts, the first line is treated as the subject of an email
and the rest of the text as the body. The blank line separating
the summary from the body is critical; various tools like `log`,
`shortlog` and `rebase` can get confused if you run the two together.

Write your commit message in the imperative: "Fix bug" and not
"Fixed bug" or "Fixes bug." This convention matches up with commit
messages generated by commands like git merge and git revert.

Explain the problem that this commit is solving. Focus on why you
are making this change as opposed to how (the code explains that).
Are there side effects or other unintuitive consequences of this
change? Here's the place to explain them.

Further paragraphs can come after blank lines.

- Bullet points are okay, too
- Use hyphen for the bullet, followed by a single space
- Use a hanging indent when bullet points exceed the 72 character
  limit.

  Keep the indent if you want to use extra paragraphs inside
  a bullet point.

Put issue tracker (backlog item) references at the bottom, examples:

See: AB#456, AB#789
Fix: AB#123  # Links and transitions the work item to the "done" state
```

## Sources
https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html<br>
https://wiki.openstack.org/wiki/GitCommitMessages<br>
https://chris.beams.io/posts/git-commit

[Back to Top](#table-of-contents)
