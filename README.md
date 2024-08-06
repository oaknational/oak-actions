# oak-actions

The `actions` folder is designed to house reusable GitHub Actions, making it easy to manage and share automation across different repositories. Each subfolder within `actions` contains a specific action with all necessary files and documentation.

#### Structure

```plaintext
actions/
├── terraform/
│   ├── action.yml
│   ├── scripts/ (if any)
│   └── README.md
```

### Terraform Action 🌍

**Location:** `actions/terraform`

**Purpose:** The Terraform action automates Terraform workflows, including applying infrastructure as code configurations.

#### Key Features

- **Infrastructure Management:** Streamlines Terraform commands in CI/CD pipelines.
- **Ease of Use:** Integrates seamlessly with your GitHub workflows.
- **Customizable:** Accepts input parameters for flexible operation.

### How to Use

```yaml
jobs:
  terraform-job:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v2
      - name: Run Terraform Action
        uses: oaknational/oak-actions/actions/terraform@main
        with:
          example_input: "value"
```

> **Note:** Replace `example_input` with the required parameters as specified in the action's `README.md`.

For more details, visit the [oaknational/oak-actions repository](https://github.com/oaknational/oak-actions).
