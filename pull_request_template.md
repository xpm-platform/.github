## Summary
<!-- What does this PR change and why? One or two sentences. Link the task if there is one. -->

---

### Author checklist
<!-- Complete before requesting review. If an item does not apply, check it and add "N/A". -->

**Scope**
- [ ] The PR has one purpose and is small enough to review in one sitting.
- [ ] The PR title and commits follow Conventional Commits, e.g. `fix(auth): handle expired token`.

**Secrets and data**
- [ ] No passwords, API keys, tokens, private keys, `.env` files or customer data in the diff.
- [ ] Logs do not contain secrets, tokens, raw prompts, document contents or personal data.

**Code**
- [ ] External input is validated, database queries are parameterized and new endpoints check permissions.
- [ ] Tests cover the changed behavior, including validation, permission and failure cases.
- [ ] Lint, type check and tests pass.

**Wider impact**
- [ ] New packages or GitHub Actions are trusted, maintained and version-pinned, and the reason is stated above.
- [ ] Database changes use a new forward-only migration. Applied migrations are not edited.
- [ ] Changes to CI/CD workflows, access or deployment settings are called out for owner review.

### Reviewer checklist
<!-- The repository's responsible reviewer confirms before approving. -->
- [ ] The author checklist is complete and matches the diff.
- [ ] I read the changed code, not only the summary.
- [ ] Security-sensitive parts (authentication, input handling, secrets, workflows) got extra attention.

<details>
<summary>Why these checks</summary>

1. **Review every change and protect the code.** NIST's Secure Software Development Framework treats code review as a core way to find vulnerabilities early and requires protecting code from unauthorized access and tampering. [NIST SP 800-218 (SSDF)](https://csrc.nist.gov/pubs/sp/800/218/final)
2. **Keep secrets out of code.** OWASP recommends catching secrets before they reach the repository and revoking and rotating any secret that leaks. [OWASP Secrets Management Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Secrets_Management_Cheat_Sheet.html)
3. **Vet and update dependencies.** OpenSSF advises evaluating dependencies before adding them, keeping them up to date and scanning them for known vulnerabilities. [OpenSSF Concise Guide for Developing More Secure Software](https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software)
4. **Reviewers own code health.** Google's engineering practices ask reviewers to check design, functionality, tests and every line they are asked to review. [Google Engineering Practices: What to look for in a code review](https://google.github.io/eng-practices/review/reviewer/looking-for.html)

</details>
