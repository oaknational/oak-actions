### Using the Terraform Action from `oaknational/oak-terraform-actions`

To use the Terraform action from the `oaknational/oak-terraform-actions` repository in your GitHub workflows, follow these steps:

1. **Create a Workflow File**: In your target repository, create a `.github/workflows` directory if it doesn't exist.

2. **Add Workflow Configuration**: Create a workflow file (e.g., `main.yml`) with the following content:

```yaml
name: oak-terraform-action

on:
  push:
    branches:
      - main

jobs:
  example-job:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Run Terraform Action from oak-terraform-actions
        uses: oaknational/oak-terraform-actions/actions/terraform@main
        with:
          example_input: "value"
```

### Explanation

- **uses: oaknational/oak-terraform-actions/actions/terraform@main**: Specifies the action from the `oak-terraform-actions` repository.
- **example_input**: Replace this with the actual input parameters required by the Terraform action 😉.

This setup allows you to incorporate the reusable Terraform action in your CI/CD workflows. For more details, visit the [oaknational/oak-terraform-actions repository](https://github.com/oaknational/oak-terraform-actions).
