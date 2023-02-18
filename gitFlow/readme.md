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
 git flow feature start contact
Switched to a new branch 'feature/contact'

Summary of actions:
- A new branch 'feature/contact' was created, based on 'develop'
- You are now on branch 'feature/contact'

Now, start committing on your feature. When done, use:

     git flow feature finish contact

❯ git branch
❯ git add .
❯ git commit -m "create file contact"
[feature/contact 7dcc72d] create file contact
 2 files changed, 71 insertions(+)
 create mode 100644 gitFlow/contact.html
 create mode 100644 gitFlow/readme.md
❯ git status
On branch feature/contact
nothing to commit, working tree clean
❯ git flow feature finish contact
Switched to branch 'develop'
Updating 59415fc..7dcc72d
Fast-forward
 gitFlow/contact.html | 12 +++++++++++
 gitFlow/readme.md    | 59 +++++++++++++++++++++++++++++++++++++++++++++++++++
 2 files changed, 71 insertions(+)
 create mode 100644 gitFlow/contact.html
 create mode 100644 gitFlow/readme.md
Deleted branch feature/contact (was 7dcc72d).

Summary of actions:
- The feature branch 'feature/contact' was merged into 'develop'
- Feature branch 'feature/contact' has been locally deleted
- You are now on branch 'develop'