# Contributing to SRPG Engine
If you are a developer and want to contribute to the development of SRPG Engine, please read this.
If you have found a bug and want to submit a minor patch or a bug report, please read this as well.

# Submitting a bug report
When submitting a bug report, make sure that the bug is local to SRPG Engine.
A bug in a SRPG_Core core or something deemed to be external is likely to be closed very fast.
If you still suspect a bug in SRPG Engine, make sure to test with several cores to make sure.

If you have troubles building SRPG Engine on Linux/BSD/OSX, make sure to paste shell output of ./configure,
as well as config.log and shell output of make. If building on Windows, just paste shell output of make.

If the issue occurs during runtime, make sure to paste SRPG Engine's verbose log.
If using Phoenix frontend, you can find log in (File -> Show Log) after running.
In console, make sure to run with verbose (-v) flag.

# Pull Requests
Outside contributions are generally only accepted in the form of a pull request. The process is very simple.
Fork SRPG Engine, make your changes, and issue a pull request on GitHub. This can all be done within the browser.
The changes are reviewed, and might be merged in. If the pull request isn't acceptable at the time,
note that it's possible to continue pushing up commits to your branch.

If you want to develop a larger feature,
we'd like to discuss this first (ideally on IRC) so that you don't risk developing something
that won't be merged. A pull request with a proof-of-concept is fine, but please indicate so.

## SRPG_Core API
If you wish to add functionality to SRPG_Core API, it can take some time to merge in, because changes
to SRPG_Core API will affect other projects as well, and we highly value API/ABI stability.
Features will only be added when deemed *necessary* for a concrete SRPG_Core to function properly.
Features will not be added on basis of hypothetical SRPG_Core implementations.

# Coding style
Having a consistent code style throughout the code base is highly valued.
Please look through the code to get a feel for the coding style.
A pull request may be asked to fix the coding style before submission.
In other cases, a pull request may be followed up with a "style nit commit".

# Copyright Headers and AUTHORS
If you have contributed to a part of a source file (a chunk of code that's written by you),
you should add yourself to the copyright header in that file.
If you have contributed significantly
(a feature, a contribution you can "name", e.g. "Added audio driver foo"), you should add yourself to AUTHORS file.
We'd like your full name and email, and which features you have been part of.

# Commit Access
Contributors who show a track record of making good pull requests over time will eventually get commit access to the repo.
This typically happens when the "overhead" of looking through pull requests over time becomes a burden.
