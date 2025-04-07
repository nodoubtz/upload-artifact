# Upload Artifact

## Overview

The `upload-artifact` repository provides a robust solution for managing and uploading artifacts in your CI/CD pipelines. This tool ensures that your build artifacts are securely stored and easily retrievable for future use.

## Features

- **Artifact Management**: Seamlessly manage your build artifacts.
- **Secure Uploads**: Ensure that your artifacts are uploaded securely.
- **Easy Integration**: Integrate with various CI/CD tools with minimal configuration.

## Getting Started

To get started with `upload-artifact`, follow the steps below:

### Prerequisites

- Node.js and npm installed on your machine.
- A GitHub repository where you want to use the `upload-artifact` action.

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/nodoubtz/upload-artifact.git
    cd upload-artifact
    ```

2. Install the dependencies:
    ```sh
    npm install
    ```

### Usage

To use the `upload-artifact` action in your GitHub Actions workflow, add the following to your workflow YAML file:

```yaml
name: Upload Artifact Example

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Set up Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '14'
    - name: Install dependencies
      run: npm install
    - name: Build project
      run: npm run build
    - name: Upload artifact
      uses: ./ # Uses an action in the root directory
      with:
        name: my-artifact
        path: path/to/artifact
```

### Configuration

You can configure the `upload-artifact` action using the following options:

- `name`: The name of the artifact to upload.
- `path`: The path to the artifact to upload.

### Contributing

We welcome contributions to the `upload-artifact` project! Please see the [CONTRIBUTING](CONTRIBUTING.md) file for more details.

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

### Support

If you have any questions or need help, feel free to open an issue in the repository or contact the maintainers.

## Acknowledgements

We would like to thank the contributors who have helped make this project better.
