# Contributing

Thank you for helping make environmental procurement comparisons easier to inspect.

## Report a reproducible issue

Include the app version, browser, expected result and observed result. Use a small synthetic example or sanitized JSON that you are permitted to share. Explain units and the comparison boundary. Do not include customer names, confidential quotations, contacts, credentials or business records in public issues.

## Make a change

1. Open an Issue explaining the user problem or calculation error.
2. Work on a branch, keeping the change focused.
3. For changes to calculations, add a worked numerical example or meaningful boundary test.
4. Run `npm test` with Node.js 22+; the project has no dependencies to install.
5. Open `index.html` in a browser and exercise the affected flow.
6. Update the relevant documentation and CHANGELOG.
7. Open a pull request with the reason, resulting behavior and validation performed.

Keep the application usable offline. Avoid adding network services or package dependencies without discussing a concrete need. Domain formulas must state assumptions and units. Distinguish implemented behavior, suggested future work and verified field results.

AI assistance is welcome. Contributors remain responsible for reviewing generated changes and should describe material AI assistance where it helps reviewers understand the work. Contributions are provided under this project's MIT license.
