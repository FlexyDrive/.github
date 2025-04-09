# Welcome to FlexyDrive's .github Repository

## Purpose

Its primary purpose is to hold default community health files and configurations that apply across multiple repositories within our organization. This helps us maintain consistency and streamline processes.

The key files managed here include:

*   **`CONTRIBUTING.md`**: Default guidelines for contributing to our projects.
*   **Issue Templates** (`.github/ISSUE_TEMPLATE/`): Standard templates for reporting bugs or suggesting features.
*   **Pull Request Templates** (`.github/PULL_REQUEST_TEMPLATE.md`): A default structure for pull request

## How It Works (GitHub Magic!)

GitHub automatically uses the files in this repository as defaults for any repository within the **[Your Organization Name]** organization that **does not** have its own version of that specific file.

For example, if `tms-backend` doesn't have its own `CONTRIBUTING.md`, GitHub will display the `CONTRIBUTING.md` from this `.github` repository when users interact with `tms-backend`.

**Note:** This repository must remain **public** for the default fallback mechanism to function correctly, even if other organization repositories are private.
