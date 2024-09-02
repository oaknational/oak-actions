# oak-terraform-actions

The `actions` folder is designed to house reusable GitHub Actions for **Terraform**, making it easy to manage and share automation across different repositories. See the Example folder to get started.

#### Structure

```plaintext
actions/
├── terraform-checks/
│   ├── action.yml
│   ├── scripts/ (if any)
│   └── README.md
```

### Terraform Actions 🌍

#### Terraform Checks

**Location:** `actions/terraform-checks`

**Purpose:** The Terraform Github Action checks your code fits the Oak standards.

#### Key Features

- **Infrastructure Management:** Streamlines Terraform commands in CI/CD pipelines.
- **Ease of Use:** Integrates seamlessly with your GitHub workflows.

### How to Use

```yaml
# Example Github Workflow file to run Terraform Check action        # Example Github Workflow file to run Terraform Check action
name: Terraform Checks

on: [push] # yamllint disable-line rule:truthy

jobs:
  terraform-lint-format:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v4
      - name: Run Terraform Action from oak-terraform-actions
        uses: oaknational/oak-terraform-actions/actions/terraform-checks@main
```

For more details, visit the [Oak Terraform Actions repository](https://github.com/oaknational/oak-terraform-actions).

You can also define the version required if necessary. See the examples folder.

# Commitlint

We're using [husky](https://github.com/typicode/husky) to create pre-commit hooks with commitlint and the [conventional commit plugin](https://github.com/conventional-changelog/commitlint).

```bash
# Example commit that passes
fix(docs): improving documentation
```
