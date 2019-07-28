# Branch Naming Convention

Folder names:
* __feature:__ All features / new functions / major refactorings are done in feature branches, which branch off of and are merged back into the develop branch (usually after some kind of peer review).
* __release:__  When enough features have accumulated or the next release time frame comes near, a new release branch is branched off of develop, which is solely dedicated to testing/bug fixing and any cleanup necessary (e.g. changing some path names, different default values for instrumentation etc.).
* __master__ Once the QA is satisfied with the quality, the release branch is merged into master (and also back to develop). This is then what is shipped/used by the customers.
* __hotfix__ If a major problem is found after release, the fix is developed in a hotfix branch, that is branched off of the master. Those are the only branches that will ever branch off of master.

Note: Any commit in master is a merge commit (either from a release or a hotfix branch) and represents a new release that is shipped to the customer.

Branch naming:

* `feature/[issue number]-Issue_name`
* `release/[release number]-Release_name`
* `hotfix/[issue number]-Issue_name`