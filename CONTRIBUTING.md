# Contributing to GigVault

First off, thank you for considering contributing to GigVault! We are building the future of the decentralized gig economy on Stellar, and community contributions are vital to our success.

## Getting Started

If you are a developer looking to contribute to GigVault, please follow these specific instructions:

### 1. Finding an Issue
Look for issues in the issues tab of the repository. 

### 2. Claiming an Issue
To claim an issue:
1. Leave a comment on the issue saying: *"I would like to work on this."*
2. **Speed is critical.** Please only request to be assigned if you have the capacity to begin working on it promptly.
3. Wait for the issue to be assigned to you.

### 3. Resolution and Rewards
* Fork the repo, write your code, and submit a Pull Request (PR).
* Reference the issue in your PR description (e.g., `Closes #12`).
* Your PR will be reviewed, approved, and merged, the issue will be marked as resolved.

## 🛠️ Standard Development Workflow

To contribute to GigVault, please follow this standard Git workflow:

### 1. Fork & Clone
Fork the repository to your own GitHub account and clone it locally:
```bash
git clone https://github.com/YOUR_USERNAME/GigVault.git
cd GigVault
```

### 2. Create a Branch
Create a new branch for your feature or bugfix. Use a descriptive name:
```bash
git checkout -b feature/add-dark-mode
# or
git checkout -b fix/escrow-validation
```

### 3. Commit Your Changes
We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification. This helps us automate changelogs and versioning.

**Examples:**
* `feat: add freighter wallet connection`
* `fix: resolve CORS issue on backend API`
* `docs: update smart contract README`
* `style: format UI components with Prettier`

### 4. Push and Open a Pull Request
Push your branch to your fork:
```bash
git push origin your-branch-name
```
Open a Pull Request against the `main` branch of the GigVault repository. 

### 5. Pull Request Guidelines
* Keep PRs small and focused on a single issue.
* Ensure all tests pass before requesting a review.
* If your PR changes the UI, please include screenshots in the PR description.
* Ensure your code passes our linting and formatting rules (`npm run lint` and `cargo fmt`).

## 🧑‍⚖️ Code of Conduct

We expect all contributors to adhere to a standard Code of Conduct. Be respectful, constructive, and kind in all PR reviews and issue discussions. Harassment or toxic behavior will not be tolerated and will result in a ban from the repository.

Thank you for helping us build GigVault! 🚀
