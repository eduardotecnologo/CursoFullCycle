$ git flow init

❯ git flow init

Which branch should be used for bringing forth production releases?

- main
Branch name for production releases: [main] main
Branch name for "next release" development: [develop]

How to name your supporting branch prefixes?
Feature branches? [feature/]
Bugfix branches? [bugfix/]
Release branches? [release/]
Hotfix branches? [hotfix/]
Support branches? [support/]
Version tag prefix? []
Hooks and filters directory? [/home/edudeveloper/developer/CursoFullCycle/.git/hooks]
Branch defult develop

$git branch
$git flow feature start welcome
Switched to a new branch 'feature/welcome'

Summary of actions:

- A new branch 'feature/welcome' was created, based on 'develop'
- You are now on branch 'feature/welcome'

Now, start committing on your feature. When done, use:

     git flow feature finish welcome
git flow release start 0.1.0
Switched to a new branch 'release/0.1.0'

Summary of actions:

- A new branch 'release/0.1.0' was created, based on 'develop'
- You are now on branch 'release/0.1.0'

Follow-up actions:

- Bump the version number now!
- Start committing last-minute fixes in preparing your release
- When done, run:

     git flow release finish '0.1.0'

git flow feature start contact
Switched to a new branch 'feature/contact'

Summary of actions:

- A new branch 'feature/contact' was created, based on 'develop'
- You are now on branch 'feature/contact'

Now, start committing on your feature. When done, use:

     git flow feature finish contact
