---
summary: In April, we paid for 129 hours of developer work, hired new heads of community and growth, and saw a huge amount of work done on Bundler and RubyGems.
---

Hello! Welcome to the monthly update. During April, our work was supported by [Handshake](https://handshake.org), [Stripe](https://stripe.com), [DigitalOcean](https://www.digitalocean.com), [Triplebyte](https://triplebyte.com/os/rubytogether), and many others.

## ruby together news

The big news of April is that we grew our team to include new roles! [Matt Solt](https://twitter.com/mattsolt) joined us as our new head of growth, and [Monica Silvestre](https://twitter.com/monicasilvestre) is our new head of community. We're super excited to work with both of them to grow Ruby Together into a bigger and better resource for the entire Ruby community.

In April, Ruby Together was supported by 60 different companies, including Sapphire member [Stripe](https://stripe.com) and Ruby member [Handshake](https://handshake.org). 1 new company joined as a member. In addition to those companies, we were supported by 62 individual members and 62 friends of Ruby Together. Thanks to all of our members for making everything that we do possible. &lt;3

## bundler news

In April, Bundler saw ongoing fixes for Windows, as well as progress on getting the test suite passing on Windows in Azure Pipelines. @deivid-rogriguez continued to clean up the test suite, making it more consistent, reliable, and organized. He also tested and repaired the mechanics for upcoming deprecations messages, ensuring that nothing will break, as well as introducing [`original_env`](https://github.com/bundler/bundler/pull/7052) to clean up previous confusion around what `clean_env` might mean.

We also fixed several other issues:
  - Bundler could sometimes try to install versions that were not compatible with the running Ruby if it was rate-limited by RubyGems.org.
  - The Bundler gemspec shipped with Ruby would sometimes be empty, because `git` is not available in the environment ruby-core uses to package default gems
  - The `clean` command would not clean up unused extensions built for git gems
  - Vendored dependencies like `fileutils` and `automatiek` were outdated
  - The `info` command was missing some intended functionality
  - The `exec` command was unable to run default gems that ship with Ruby

Finally, in extremely exciting news, the process of merging Bundler and RubyGems has been [written down, discussed, and approved](https://github.com/bundler/rfcs/pull/18/) by both the RubyGems and Bundler maintainer teams! We'll keep you updated as we make progress on combining Bundler and RubyGems together.

This month, Bundler gained 187 new commits, contributed by 10 authors. There were 2,613 additions and 1,743 deletions across 142 files.

## rubygems.org news

Over on RubyGems.org, the yank rate limit was increased, password resets were updated to include two factor authentication, we added a webhook for yanking versions (thanks, @greysteil!), the Japanese translation was updated, and several other smaller issues were resolved.

This month, Rubygems.org gained 36 new commits, contributed by 9 authors. There were 668 additions and 172 deletions across 43 files.

## rubygems news

Various issues were resolved in RubyGems this month, including:

  - Always expanding globbed file paths
  - Setting permissions for non-owners on installed files
  - Fixing `Gem::Requirement` so `~> 5.2` and `~> 5.2.0` are different, as intended
  - Using `%x{}` for better Windows compatibility
  - Removed a circular require in `rubygems/text`
  - Added missing gem wrapper for default gem Bundler
  - Bring back prompt for version if `uninstall` has multiple version options

In addition to those issues, many old deprecations and other legacy code and test issues were cleaned up.

This month, Rubygems gained 108 new commits, contributed by 9 authors. There were 618 additions and 219 deletions across 48 files.

## gemstash news

Gemstash was pretty quiet this month, and only saw the test suite bumped to run against the latest versions of Ruby and some style fixes. There were 8 new commits from 4 contributors, including 8 additions and 8 deletions across 4 files.

## budget &amp; expenses

In April, we saw $13,057 in total income and $31,285.63 in total expenditure, to fund a total of 128.7 hours of developer work on Ruby open source.

* $10,000 for 66.7 hours worked on Bundler at $150/hour
* $1,562.50 for 10.4 hours worked on RubyGems.org at $150/hour
* $4,678.12 for 31.2 hours worked on RubyGems at $150/hour
* $2,559.38 for 17.1 hours worked on other OSS and devtools at $150/hour
* $487.50 for 3.3 hours worked on The Ruby Toolbox at $150/hour
* $77.18 on dedicated servers for RubyBench.org
* $441.01 on payment processing fees
* $7,023.65 on company overhead like hosting, services, software, hardware, taxes, etc
* $1,952.33 on accounting, copywriting, design, and other professional services
* $2,503.96 on marketing, evangelism, and community outreach


Until next time,<br>
André and the Ruby Together team
