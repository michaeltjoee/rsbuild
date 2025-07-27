# RsStack

A pnpm workspace for managing multiple packages and applications.

## Structure

```
RsStack/
├── apps/          # Applications
├── packages/      # Shared packages/libraries
├── package.json   # Root workspace configuration
├── pnpm-workspace.yaml
└── README.md
```

## Getting Started

### Prerequisites

- Node.js >= 18.0.0
- pnpm >= 8.0.0

### Installation

1. Install dependencies:
   ```bash
   pnpm install
   ```

2. Build all packages:
   ```bash
   pnpm build
   ```

3. Run development mode:
   ```bash
   pnpm dev
   ```

## Available Scripts

- `pnpm build` - Build all packages
- `pnpm dev` - Start development mode for all packages
- `pnpm test` - Run tests for all packages
- `pnpm lint` - Run linting for all packages
- `pnpm clean` - Clean build artifacts

## Adding New Packages

### Adding a Package

1. Create a new directory in `packages/`:
   ```bash
   mkdir packages/my-package
   cd packages/my-package
   ```

2. Initialize the package:
   ```bash
   pnpm init
   ```

3. Add the package to the workspace by running from the root:
   ```bash
   pnpm install
   ```

### Adding an Application

1. Create a new directory in `apps/`:
   ```bash
   mkdir apps/my-app
   cd apps/my-app
   ```

2. Initialize the application:
   ```bash
   pnpm init
   ```

3. Add the application to the workspace by running from the root:
   ```bash
   pnpm install
   ```

## Workspace Configuration

The workspace is configured via `pnpm-workspace.yaml` and includes:

- `packages/*` - Shared libraries and packages
- `apps/*` - Applications

## Development

This workspace supports:
- TypeScript
- Shared dependencies
- Cross-package development
- Unified build and test processes

## Contributing

1. Create a new branch for your feature
2. Make your changes
3. Run tests: `pnpm test`
4. Run linting: `pnpm lint`
5. Submit a pull request 