---
date: 2020-09-18 04:37:02
layout: post
title: "What is GitHub CLI and How to use?"
subtitle: "You can now access your GitHub through your Command Line"
description: "Take GitHub to your Terminal"
image: https://devskrate.github.io/assets/blog-banners/github-cli-stable.jpg
optimized_image: https://devskrate.github.io/assets/blog-banners/optimized/github-cli-stable.webp
author: nikhil
category: [dev]
tags: [github, git, cli]
is_generated: false
---

GitHub CLI brings GitHub to your terminal. It reduces context switching, helps you focus, and enables you to more easily script and create your own workflows. Earlier this year, GitHub announced the beta of GitHub CLI. Since it released the beta, users have created over **250,000 pull requests**, performed over **350,000 merges**, and created over **20,000 issues** with GitHub CLI. And finally, GitHub CLI is out of beta and available to download on [Windows, macOS, and Linux](https://cli.github.com/).

Take a breif look at all the **GitHub CLI Commands** [here](https://cli.github.com/manual/)

#### With GitHub CLI 1.0, you can:

- Run your entire GitHub workflow from the terminal, from issues through releases
- Call the GitHub API to script nearly any action, and set a custom alias for any command
- Connect to GitHub Enterprise Server in addition to GitHub.com

### From issue to release:

Use GitHub CLI for your entire GitHub workflow.

- Clone the repository you want to work with using `gh repo clone owner/repo`.
- Find the next thing you need to work on with `gh issue status` or `gh issue list --assignee billygriffin`.  
  ![gh issue list on github cli app](https://devskrate.github.io/assets/images/git/cli-1.png)
- When you’ve finished adding that feature or fixing that bug, use `gh pr create` to create your pull request on GitHub.  
  ![gh issue list on github cli app](https://devskrate.github.io/assets/images/git/cli-2.png)
- And your teammate can check out your pull request using `gh pr checkout 1337`, view the diff with `gh pr diff`, and even provide a lightweight review using `gh pr review`.  
  ![gh issue list on github cli app](https://devskrate.github.io/assets/images/git/cli-3.png)
- After the pull request is approved, you can make sure all your tests are passing with `gh pr checks`, and then go ahead and merge it right from your terminal with `gh pr merge`. GitHub CLI will even offer to delete your branch locally and on GitHub.com after the merge.  
  ![gh issue list on github cli app](https://devskrate.github.io/assets/images/git/cli-4.png)
- And when you’re ready to cut your next release, just use `gh release create [tag name]` and make your creation available to the world without ever leaving your command line!

### Make GitHub CLI your own with aliases and gh api

GitHub CLI now allows you to create aliases for any command using `gh alias set`. And with the powerful `gh api` allowing you to access the GitHub API directly, there’s no limit to what you can do with `gh`. Commands are also easily composable.

### GitHub CLI is available for GitHub Enterprise Server

Finally, you can use GitHub CLI with repositories hosted on GitHub Enterprise Server 2.20+. This has been the most frequent request since we announced the beta, and we’re excited that more and more people using GHES will be able to also use GitHub CLI.
