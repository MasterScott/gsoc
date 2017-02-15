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
- [@MikeMcQuaid](https://github.com/mikemcquaid) (mike@mikemcquaid.com)
- [@mistydemeo](https://github.com/mistydemeo) (mistydemeo@gmail.com)
- [@woodruffw](https://github.com/woodruffw) (william@yossarian.net)
- [@jawshooah](https://github.com/jawshooah) (hagins.josh@gmail.com)
- [@tdsmith](https://github.com/tdsmith)
- [@ilovezfs](https://github.com/ilovezfs)
- more to follow

Mentorship happens privately on our Homebrew maintainer's Slack and publicly on GitHub pull requests. Each student and project will be assigned a mentor but all students will work with all mentors.

## Technologies Used and Requirements

Homebrew is written in Ruby, runs on Apple's macOS operating system and uses Git and GitHub for version control and updates. You do not need to have used any of these before but must have access to a Mac and be willing to learn Ruby, Git and GitHub.

## Ideas
These are suggestions that we think would make good Outreachy or Google Summer of Code projects. Feel free to open an issue if you wish to discuss or propose your own idea.

### Emit warnings for mistyped options (https://github.com/Homebrew/homebrew/issues/8937)
Currently providing options that don't exist for Homebrew commands silently ignores them. These should instead print a warning to user. This project will involve adding a new DSL for commands in Homebrew/brew to declare what options they accept and migrating all uses of `ARGV.include?` (and potentially all monkeypatching of `ARGV` itself) to this new DSL and abstraction.

### Improve brew tests coverage percentage by writing more tests
Homebrew's code coverage for `brew tests` is poor. This could be improved by writing more unit and integration tests for Homebrew and generally improving our test suite to make it easier and faster to run and write tests. You should have experience with unit testing to apply and will be writing tests in RSpec.

### Better support pinning to a major/minor version with Homebrew Bundle and `@`-versioned formulae
Users of Homebrew Bundle may wish to pin to a particular version of a package without knowing about versioned formulae. These formulae should be used automatically when possible. Inspiration can be taken from RubyGems and a `Brewfile.lock` file could be generated.

### Complete public API documentation
Not all of Homebrew's public APIs are documented. These should all be documented and the presentation optimised to make it easier for people writing new formulae. This will involve figuring out how existing code works, what APIs can be made private or hidden and discussing with Homebrew maintainers how best to describe a given API.

### Add features to resources
Homebrew provides `resource` blocks for lightweight formulae-like things within formulae. These should be extended to support patching with `patch do` blocks, inferring versions from the formula, sharing cached resource downloads when the same file is downloaded between formulae, being conditionally downloaded and other improvements you suggest.

### Add `variant`s as an `option` alternative
A `variant do` block should allow specifying dependencies, resources, exclusivity with other `variant`s and other DSL methods inside itself and can be specified like an option. This will require working with both Homebrew/brew code and Homebrew/homebrew-core formulae code to adapt some existing code to use variants rather than options.

### Cache subdirectories for formulae and versions for speedup
The `HOMEBREW_CACHE` should be rearranged to have a `Cellar`-like hierarchy with subdirectories for formulae and then versions, resources and patches. This should be used to speed up `brew cleanup` so that it can be implemented in Bash and run automatically to clean up now
irrelevant files to free up disk space.

### Port `brew audit` rules to RuboCop
`brew audit` now runs RuboCop custom cops to enforce and automatically fix Homebrew coding style guidelines within supported editors and using the `rubocop` tool. All possible `brew audit` rules (e.g. those using `regex` matches) should be migrated to use RuboCop rather than custom `brew audit` logic.

### Other Ideas
You may also get inspiration from [open `help wanted` issues on Homebrew/brew](https://github.com/homebrew/brew/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22). Please discuss any of these with us before submission to maximise your changes of being accepted.
