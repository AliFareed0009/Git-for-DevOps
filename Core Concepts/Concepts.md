## Key Definitions
Throughout this cheat sheet, you’ll find git-specific terms and jargon being used. Here’s a run-down of all the terms you may encounter

### Basic definitions
- Local repo or repository: A local directory containing code and files for the project
- Remote repository: An online version of the local repository hosted on services like GitHub, GitLab, and BitBucket
- Cloning: The act of making a clone or copy of a repository in a new directory
- Commit: A snapshot of the project you can come back to
- Branch: A copy of the project used for working in an isolated environment without affecting the main project
- Git merge: The process of combining two branches together

### More advanced definitions
- .gitignore file: A file that lists other files you want git not to track (e.g. large data folders, private info, and any local files that shouldn’t be seen by the public.)
- Staging area: a cache that holds changes you want to commit next.
- Git stash: another type of cache that holds unwanted changes you may want to come back later
- Commit ID or hash: a unique identifier for each commit, used for switching to different save points.
- HEAD (always capitalized letters): a reference name for the latest commit, to save you having to type Commit IDs. HEAD~n syntax is used to refer to older commits (e.g. HEAD~2 refers to the second-to-last commit).