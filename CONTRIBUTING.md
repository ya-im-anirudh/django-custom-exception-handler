# Contributing Guidelines

Thank you for considering contributing to this Django Python package\! 🎉 We appreciate your help in making this project better. Please read these guidelines carefully to keep our workflow consistent, clean, and easy to maintain.

-----

## 📌 How to Contribute

1.  **Fork the Repository**

      * Click the "Fork" button on the repo page.

2.  **Clone Your Fork**

    ```bash
    git clone https://github.com/<your-username>/<repo-name>.git
    cd <repo-name>
    ```

3.  **Set up the Development Environment**
    It's recommended to work in a virtual environment.

    ```bash
    # Create a virtual environment
    python -m venv venv

    # Activate it
    source venv/bin/activate  # On macOS/Linux
    venv\Scripts\activate      # On Windows

    # Install dependencies
    pip install -e .
    ```

4.  **Create a Branch**
    Branch names must describe the work: `feat/feature-name` → New features, `fix/bug-description` → Bug fixes, `docs/topic` → Documentation changes.

    ```bash
    git checkout -b fix/prevent-template-tag-error
    ```

5.  **Make Changes**
    Keep commits small and focused on one logical change.

6.  **Write a Good Commit Message**
    Use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/):

    ```
    <type>(optional scope): <short summary>

    - Change 1
    - Change 2
    - Change 3

    Closes #issue-number
    ```

    **Types:**

      * **feat** → New feature
      * **fix** → Bug fix
      * **docs** → Documentation changes only
      * **style** → Formatting, no logic change
      * **refactor** → Code restructuring without behavior change
      * **perf** → Performance improvement
      * **test** → Adding/updating tests
      * **build** → Build system changes
      * **chore** → Maintenance tasks

    **Example:**

    ```
    fix(templates): prevent error when context is missing key

    - Added a check in the custom template tag to handle missing keys gracefully.
    - Updated the test suite to include a test case for this specific error scenario.

    Closes #42
    ```

7.  **Test Your Changes**
    Run the test suite to ensure your changes haven't introduced any regressions and that new functionality is properly tested.

    ```bash
    pytest
    ```

8.  **Push to Your Fork**

    ```bash
    git push origin fix/prevent-template-tag-error
    ```

9.  **Open a Pull Request**
    Go to the original repo and click "New Pull Request." Fill in all required PR template fields.

-----

## 🛠 Code Style

  * **Python/Django:**

      * Adhere strictly to **PEP 8** standards.
      * Use code formatters like **Black** and **isort** to maintain a consistent style.
      * Follow the **Don't Repeat Yourself (DRY)** principle.
      * Comment complex logic and provide docstrings for public functions and classes.

  * **Package Specific:**

      * Prioritize API stability and backward compatibility.
      * Add tests for all new functionality and bug fixes.
      * Ensure all public-facing code (e.g., templatetags, management commands, models) is well-documented.

-----

## ✅ Pull Request Requirements

  * **Title:** Must follow the commit message format.
  * **Description:** List all major changes in bullet points.
  * **Tests:** New features and bug fixes **must** include tests that pass.
  * **Documentation:** Update the package's documentation to reflect any new features or API changes.
  * **Linked Issues:** Use `Closes #issue-number` if applicable.

-----

## 🔍 Review Process

  * Maintainers will review your changes within a few days.
  * You may be asked to make changes before a merge.
  * Once approved, your branch will be merged into `main`.

-----

## 📜 License

By contributing, you agree that your contributions will be licensed under the same license as the repository.

Happy coding\! 🚀
