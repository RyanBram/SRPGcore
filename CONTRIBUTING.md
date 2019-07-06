# Contributing to SRPG Engine
If you have Javascript programming skill and want to contribute to the development of SRPG Engine, please read this.
If you have found a bug and want to submit a minor patch or a bug report, please read this as well.

## Submitting a bug report
When submitting a bug report, make sure that the bug is local to SRPG Engine.
A compatibility issue with other plugins or something deemed to be external are not on our current priority.
If you still suspect a bug in SRPG Engine, test it with clean project to make sure.

If you have troubles using SRPG Engine, please use the Demo as your template and start by creating something simple before jumping to more complex mechanism.
If the issue occurs during runtime, make sure to explain clearly how to reproduce the issue.

## Suggesting new features
Adding fancy new features to SRPG Engine is a nice thing. But we also have real life, which mean we should give priority which feature that will be implemented first. Usually we prefer something more general purpose and have direct impact with how SRPG Battle should be. Visual customization, such as custom windowskin or custom GUI or something that too specific will be better if made as extension instead of bundled as part of SRPG_Core. We want to make the SRPG_Core as generic as possible by re-using part of MV Corse scripts to maintain compatibility with most plugins and extensions.

## Contribution to SRPG_Core.js
Contributions to SRPG_Core are generally accepted in the form of a pull request.
The process is very simple, fork SRPG Engine, make your changes, and issue a pull request on GitHub. This can all be done within the browser.
The changes are reviewed, and might be merged in. If the pull request isn't acceptable at the time, you can message us.

If you want to develop a larger feature or change SRPG_Core functions, we'd like to discuss this first using issue tracker, so that you don't risk developing feature that on being developed or feature that should not be part of Core, but can be made as extension. A pull request with a proof-of-concept is fine, but please indicate so.

If you wish to add radical change to SRPG_Core API, it can take some time to merge in, because changes to SRPG_Core API will affect extensions as well, and we highly value API/ABI stability.
Features will only be added when deemed *necessary* for a concrete SRPG_Core to function properly.

## Contribution as SRPG Engine extension
Nice. This is how generally contribution to the project.
We hope that by opening this engine to public, it can become a "side" engine for RPG Maker MV. Any additonal feature between extension should always keep compatibility with other plugins in mind. We intend to reduce compatibility issue between plugins and it should become new tradition in developing MV plugins.

If you want to make extension, you can choose how you will contribute to the project:
### 1. As part of SRPG Engine project
If you want to donate your extension to be part of SRPG Engine, you will retain your credits in header files, but you also give this project maintainer right to do whatever necessary for any code that have been submitted by you. Your extension will be hosted in SRPG Engine main repository as official extension.
We kindly ask any extension that will be made as official extension to follow SRPG Engine coding style and naming convention. The name of plugins should prefixed with SRPG_ and continued with name that indicate its function without adding author initial name, e.g we cannot accept **SRPG_RB_CustomMenu.js** , please rename it with **SRPG_CustomMenu.js** by ommiting **RB_** part.

### 2. As external extension
In case you have difference Term of Conditions than this project, we still list your contribution as part of external extension. We will put your website in our extension list, so any user can find your extension easily.

## Coding style
Having a consistent code style throughout the code base is highly valued.
Please look through the code to get a feel for the coding style.
A pull request may be asked to fix the coding style before submission.
In other cases, a pull request may be followed up with a "style nit commit".

## Copyright Headers and AUTHORS
If you have contributed to a part of a source file (a chunk of code that's written by you), you should add yourself to the copyright header in that file.
If you have contributed significantly (a feature, a contribution you can "name", e.g. "Added audio driver foo"), you should add yourself to AUTHORS file.
We'd like your full name and email, and which features you have been part of.

## Commit Access
Contributors who show a track record of making good pull requests over time will eventually get commit access to the repo.
This typically happens when the "overhead" of looking through pull requests over time becomes a burden.
