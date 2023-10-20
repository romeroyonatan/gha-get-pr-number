## Get the PR Number Action

This GitHub Action is designed to extract the Pull Request (PR) number for both `pull_request` and `merge_group` event types.

### 🚀 Usage

To utilize this action in your workflow, follow the steps below:

1. Add the action to your `.github/workflows/[your_file].yml`.

```
on: [pull_request, merge_group]

jobs:
  your-job:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Get PR Number
      id: get-pr-number
      uses: mgaitan/gha-get-pr-number

    - name: Print PR Number
      run: echo "The PR Number is ${{ steps.get-pr-number.outputs.number }}"
```


### 📦 Output

- **number**: The extracted PR number.

### 🔧 Contribution

If you encounter any issues or have improvements in mind, please feel free to open an issue or submit a pull request.

### 📜 License

MIT License. 
