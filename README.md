# Homebrew's Outreachy and Google Summer of Code
These ideas are suggestions that we think would make good Outreachy or Google Summer of Code projects. They are only meant to be a starting point. Check out our proposal template, and feel free to open an issue to ask questions or discuss other ideas.

## Application Instructions

In your application tell us:

1. Who you are: your name and how we contact you (e.g. email)
2. What idea are you proposing: which of our ideas is it or describe in detail if it's your own
3. How will you implement it: provide a detailed work timeline that breaks the project into one or two week milestones
4. Why you: link to a previous Homebrew pull-request you've submitted

Homebrew is actively seeking to diversify our contributors and especially welcome applications from women from all backgrounds and people of colour.

### Google Summer of Code
Please read and apply via https://summerofcode.withgoogle.com/get-started/.

### Outreachy
Please read https://wiki.gnome.org/Outreachy/#Submit_an_Application and apply via https://outreachy.gnome.org/?q=program_home&prg=6.

## Mentors
- Mike McQuaid (mike@mikemcquaid.com)
- More to follow

## Technologies Used

Homebrew is written in Ruby, runs on Apple's macOS operating system and uses Git and GitHub for version control and updates. You do not need to have used any of these before but must have access to a Mac and be willing to learn Ruby, Git and GitHub.

## Ideas
These are suggestions that we think would make good Outreachy or Google Summer of Code projects. Feel free to open an issue if you wish to discuss or propose your own idea.

### Emit warnings for mistyped options (https://github.com/Homebrew/homebrew/issues/8937)
Currently providing options that don't exist for formulae or Homebrew commands silently ignores them. These should instead print a warning to user. This project will involve tracking options for formulae and their dependencies and a new DSL for commands to declare what options they accept.

### Improve brew tests coverage percentage by writing more tests
Homebrew's code coverage for `brew tests` is poor. This could be improved by writing more unit and integration tests for Homebrew and generally improving our test suite to make it easier and faster to run and write tests.

### Better support pinning to a major/minor version with Homebrew Bundle/Homebrew Versions
Users of Homebrew Bundle may wish to pin to a particular version of a package without knowing about versioned formulae. These formulae should be used automatically when possible.

### Complete public API documentation
Not all of Homebrew's APIs are documented. These should all be documented and the presentation optimised to make it easier for people writing new formulae.

### Add features to resources
Homebrew provides `resource` blocks for lightweight formulae-like things within formulae. These should be extended to support patching with `patch do` blocks, sharing cached resource downloads and other improvements you suggest.

### Add `variant`s as an `option` alternative
A `variant` block should allow specifying dependencies, resources and other DSL methods inside itself and can be specified like an option.

### Other Ideas
You may also get inspiration from [open `help wanted` issues on Homebrew/brew](https://github.com/homebrew/brew/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22). Please discuss any of these with us before submission to maximise your changes of being accepted.
