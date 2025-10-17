# Bruno Test RP

Sample Bruno API testing repository demonstrating Bruno as an offline-first alternative to Postman.

## Quick Start

### Prerequisites

- **Bruno App**: Install from [usebruno.com](https://www.usebruno.com/downloads) or via Homebrew:
  ```bash
  brew install bruno
  ```

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/neil-alday-rp/Bruno_Test_RP.git
   cd Bruno_Test_RP
   ```

2. **Open collection in Bruno**
    - Launch Bruno application
    - File → Open Collection
    - Select the cloned directory

3. **Configure environment**
    - Select an environment from the dropdown
    - Update variables as needed (host, credentials, etc.)

### Running Requests

**Via Bruno App:**
- Open any request and click "Send"
- Auth tokens automatically persist via post-request scripts



## Key Features Demonstrated

- **Git-friendly storage**: Collections stored as `.bru` files
- **Environment management**: Multiple environments per collection
- **Authentication flow**: Auto-capture and persist auth tokens
- **Post-request scripts**: Response validation and variable extraction
- **Secret management**: Flag variables as secrets (not tracked in git)

## Important Notes

### ⚠️ Environment Variables

**CRITICAL**: Do not commit environment files with sensitive credentials.

- Environment files contain your local configurations
- Be careful with `git add` to avoid staging environment changes
- Flag sensitive values as "secrets" in Bruno

### Scripting Syntax

Bruno uses different syntax from Postman:

```javascript
// Postman
pm.environment.set("token", value);

// Bruno
bru.setEnvVar("token", value);
```

See individual request scripts for examples.

## Repository Structure

```
.
├── collection-name/
│   ├── environments/
│   │   ├── local.bru
│   │   └── staging.bru
│   ├── requests/
│   │   ├── auth/
│   │   │   └── login.bru
│   │   └── api/
│   │       └── example.bru
│   └── bruno.json
└── README.md
```

## Resources

- **Documentation**: Full guide available in Confluence
- **Official Docs**: [docs.usebruno.com](https://docs.usebruno.com)
- **Bruno vs Postman**: [Comparison](https://www.usebruno.com/compare/bruno-vs-postman)

## Contributing

1. Create a feature branch
2. Make your changes in Bruno
3. Commit and push changes
4. Open a pull request

*Note: API test changes should go through PR review process.*
