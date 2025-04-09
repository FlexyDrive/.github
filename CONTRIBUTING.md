# Contributing to FlexyDrive Projects 🤝

Please take a moment to review this document to understand our general contribution process.

## Getting Started

*   **Reporting Issues:** If you find a bug or have a problem, please check the existing issues in the relevant project repository first. If it hasn't been reported, create a new issue using the available templates (if provided). Describe the issue clearly, including steps to reproduce if applicable.
*   **Suggesting Enhancements:** For new features or improvements, feel free to open an issue to discuss your idea first. This helps ensure it aligns with the project's goals before significant effort is invested.

---

## Contribution Workflow

As members of the FlexyDrive organization working on private repositories, we generally follow this workflow:

1.  **Clone:** Ensure you have the latest version of the specific project repository cloned locally.
    ```bash
    # If you haven't cloned it yet:
    git clone <repository_url>
    cd <repository_name>

    # If you have it cloned, ensure it's up-to-date:
    git checkout main
    git pull origin main
    ```
2.  **Branch:** Create a new branch **directly within the main repository** for your changes. Name it descriptively using a convention like `type/short-description` or `username/type/short-description`.
    ```bash
    # Example: Create and switch to a new branch
    git checkout -b feat/user-profile-page
    # Or, using username prefix:
    # git checkout -b your_username/fix/auth-bug-123
    ```
3.  **Develop:** Make your code changes, ensuring you adhere to any project-specific style guides or testing requirements (check the project's README or specific CONTRIBUTING guide if it exists).
4.  **Commit:** Commit your changes locally using clear, conventional commit messages (see below).
5.  **Push:** Push your **new branch** to the main repository on GitHub (`origin`).
    ```bash
    git push -u origin feat/user-profile-page # Or your branch name
    ```
6.  **Pull Request:** Open a pull request **within the same repository** from your newly pushed branch (`feat/user-profile-page`) to the repository's main branch (`main`). Provide a clear title and description, linking any relevant issues.

---

## Commit Message Guidelines (Conventional Commits) ✨

We use **Conventional Commits** for our commit messages. This standard format helps us automate changelog generation, determine semantic version bumps, and makes the commit history much easier to read and understand.

**Specification:** [https://www.conventionalcommits.org/]

**Format**
  ```text
  <type>[optional scope]: <description>

  [optional body]

  [optional footer(s)]
  ```

**Common Types:**

Here are the most common types used in our commit messages, based on the Conventional Commits specification. Choosing the correct type is important as it directly influences automated version bumping and changelog generation.

*   **`feat`**: (Features)
    *   **Description:** Used when introducing a new feature or functionality visible to the end-user or consumer of the API/application.
    *   **Example:** `feat: add user profile settings page`

*   **`fix`**: (Bug Fixes)
    *   **Description:** Used when patching a bug in the existing codebase that affects the end-user or consumer.
    *   **Example:** `fix: correct price calculation for discounted items`

*   **`docs`**: (Documentation)
    *   **Description:** Used for changes solely affecting documentation files (e.g., README, guides, comments within code that only explain).
    *   **Example:** `docs: explain environment variable configuration`

*   **`style`**: (Code Style)
    *   **Description:** Used for changes that do not affect the meaning or logic of the code (e.g., whitespace, formatting, semicolons, linting fixes).
    *   **Example:** `style: apply standard code formatting rules`

*   **`refactor`**: (Code Refactoring)
    *   **Description:** Used when restructuring existing code without changing its external behavior, fixing bugs, or adding features (e.g., improving readability, extracting methods, simplifying logic).
    *   **Example:** `refactor: extract authentication logic into separate module`

*   **`perf`**: (Performance Improvements)
    *   **Description:** Used for code changes that specifically improve performance.
    *   **Example:** `perf: optimize database query for faster loading`

*   **`test`**: (Tests)
    *   **Description:** Used when adding missing tests or correcting existing tests. Does not include changes to the source code itself.
    *   **Example:** `test: add unit tests for user service validation`

*   **`build`**: (Build System)
    *   **Description:** Used for changes that affect the build system, build process, or external dependencies (e.g., updating build scripts, package manager configs, Dockerfiles).
    *   **Example:** `build: update Go version in Dockerfile`

*   **`ci`**: (Continuous Integration)
    *   **Description:** Used for changes to CI configuration files and scripts (e.g., GitHub Actions workflows, Travis CI, Jenkins config).
    *   **Example:** `ci: add commit linting check to pull request workflow`

*   **`chore`**: (Chores)
    *   **Description:** Used for routine maintenance, updates, or other changes that don't fit into the other categories and don't modify source or test files (e.g., updating dependencies versions, managing `.gitignore`).
    *   **Example:** `chore: update dependency xyz to latest version`

*This list covers common types. For the complete specification, refer to [https://www.conventionalcommits.org/](https://www.conventionalcommits.org/).*

**Examples:**

```text
feat: allow users to upload profile pictures
```

```text
fix(api): correct calculation for order totals
# Closes #123
```

```text
fix(dashboard): prevent chart legend overlapping on smaller screens

Corrects a CSS layout issue where the chart legend on the main dashboard
would overlap with the chart itself on viewports narrower than 768px.
Introduced flex-wrap property to the legend container and adjusted
margins for better responsiveness.

This bug made the legend unreadable on mobile devices and smaller tablets.

Tested on Chrome, Firefox, and Safari responsive modes.

Reviewed-by: Frontend Team <frontend@example.com>
Fixes: #901
```

---

## Pull Request Process

Once you've pushed your branch with your changes, you're ready to open a Pull Request (PR) to merge them into the main branch.

1.  **Open the PR:** Navigate to the main repository page on GitHub. You should see a prompt to create a PR from your recently pushed branch. Click it, or manually open a new PR comparing your branch against the repository's default branch (usually `main`).
2.  **Clear Title and Description:**
    *   Use a concise, descriptive title that reflects the changes (often similar to your primary commit message).
    *   Fill out the description template (if provided). Explain the "what" and "why" of your contribution. What problem does it solve? How does it address it?
3.  **Link Issues:** If your PR addresses one or more existing GitHub issues, link them using keywords like `Closes #123`, `Fixes #456`, or `Resolves #789` in the PR description. This automatically closes the linked issues when the PR is merged.
4.  **Draft PRs (Optional):** If your work is still in progress but you'd like early feedback or visibility, open the PR as a [Draft Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests#draft-pull-requests). Mark it as "Ready for Review" when it's complete.
5.  **Automated Checks:** Ensure all automated checks (like linting, tests, builds) triggered by the PR pass successfully. Address any failures before requesting a review.
6.  **Request Review:** Once the PR is ready and checks are passing, request a review from relevant team members or code owners if applicable.
7.  **Respond to Feedback:** Be responsive to comments and suggestions during the code review process. Discuss feedback constructively and push updates to your branch as needed (they will automatically appear in the PR).
8.  **Approval and Merge:** Once the PR is approved and all checks pass, a maintainer will merge it into the main branch. Congratulations!

**Important:** Do not merge your own PRs unless specifically agreed upon within your team's workflow. Let the review process complete.

---

## Project-Specific Guidelines

**Important:** While this document provides general guidelines for the organization, individual repositories **may have their own `CONTRIBUTING.md` file** with more specific instructions regarding setup, testing, style guides, or technology choices.

If a project has its own `CONTRIBUTING.md`, please adhere to its guidelines. These project-specific files should ideally **link back** to this organization-wide document for the common standards (like commit messages and code of conduct) before detailing their unique requirements. Always check the specific repository you are working in for its own contributing guide first.
