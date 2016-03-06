# Homebrew's Google Summer of Code
These ideas are suggestions that we think would make good Google Summer of Code projects. They are only meant to be a starting point. Check out our proposal template, and feel free to open an issue to ask questions or discuss other ideas.

## Application Instructions

In your application tell us:

1. Who you are: your name and how we contact you (e.g. email)
2. What idea are you proposing: which of our ideas is it or describe in detail if it's your own
3. How will you implement it: provide a detailed work timeline that breaks the project into one or two week milestones
4. Why you: link to any previous GitHub pull-requests you've submitted to any project (ideally Homebrew-related)

Homebrew is actively seeking to diversify our contributors and especially welcome applications from women from all backgrounds and people of colour.

## Ideas
These are suggestions that we think would make good Google Summer of Code projects. Feel free to open an issue if you wish to discuss or propose your own idea.

### Emit warnings for mistyped options (https://github.com/Homebrew/homebrew/issues/8937)
Currently providing options that don't exist for formulae or Homebrew commands silently ignores them. These should instead print a warning to user. This project will involve tracking options for formulae and their dependencies and a new DSL for commands to declare what options they accept.

### Better support HEAD formulae (https://github.com/Homebrew/homebrew/issues/13197)
Currently HEAD formulae (those installed from version control branches rather than archives/tags) cannot be upgraded. Instead of using `HEAD` as the version instead e.g. `HEAD-r123` with a revision number should be used to allow HEAD formulae to be upgraded.

### Better integrate with Homebrew cask (https://github.com/caskroom/homebrew-cask/issues/14384)
Homebrew Cask and Homebrew with to be better integrated. Cask's core code should be moved into Homebrew core and commands such as e.g. `brew deps` and `brew fetch` should accept casks as arguments (rather than just formulae).

### Improve brew tests coverage percentage by writing more tests
Homebrew's code coverage for `brew tests` is poor. This could be improved by writing more unit and integration tests for Homebrew and generally improving our test suite to make it easier and faster to run and write tests.

### Better support pinning to a major/minor version with Homebrew Bundle/Homebrew Versions
Users of Homebrew Bundle may wish to pin to a particular version of a package without knowing about the Homebrew Versions tap. There should be a DSL added to Homebrew core, bundle and versions to allow this to be handled smoothly.

### Complete public API documentation
Not all of Homebrew's APIs are documented. These should all be documented and the presentation optimised to make it easier for people writing new formulae.

### Add features to resources
Homebrew provides `resource` blocks for lightweight formulae-like things within formulae. These should be extended to support patching with `patch do` blocks, sharing cached resource downloads and other improvements you suggest.

### Add `variant`s as an `option` alternative
A `variant` block should allow specifying dependencies, resources and other DSL methods inside itself and can be specified like an option.

### Try and build and upload pull request bottles using Travis CI
Homebrew uses Travis CI for some of our CI builds. We cannot currently build and upload pull request bottles using Travis CI but it would be good to try and do so so we can rely more on Travis CI and less on our own infrastructure. 
