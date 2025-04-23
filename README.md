# TypeScript SDK Starter Template

This is a starter template for creating TypeScript SDKs with a complete development environment and build configuration.

## Features

- TypeScript configuration for library development
- Testing setup with Mocha, Chai, and Sinon
- Linting with ESLint and Prettier
- Build system with source maps and declaration files
- Proper module structure for SDK development
- Assets handling

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- pnpm (v10 or higher)

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/ts-sdk-plate.git
cd ts-sdk-plate

# Install dependencies
pnpm install
```

### Development

The project has the following structure:

```
ts-sdk-plate/
├── src/                   # Source code
│   ├── assets/            # Static assets
│   ├── constants.ts       # Constants
│   ├── hello.ts           # Example module
│   ├── index.ts           # Main entry point
│   └── types.ts           # TypeScript interfaces
├── test/                  # Test files
│   ├── sdk-test.spec.ts   # SDK tests
│   └── setup.ts           # Test setup
├── .editorconfig          # Editor configuration
├── .eslintrc.js           # ESLint configuration
├── .prettierrc            # Prettier configuration
├── tsconfig.json          # TypeScript configuration
└── tsconfig.build.json    # Build-specific configuration
```

### Scripts

```bash
# Build the SDK
pnpm build

# Run tests
pnpm test

# Lint code
pnpm lint

# Fix linting issues
pnpm lint:fix

# Format code with Prettier
pnpm prettier
```

## Using the SDK

After building, you can import the SDK in your projects:

```typescript
import { hello_world, API_URL } from '@ts-sdk/plate';

// Use the SDK
hello_world(); // Logs "Hello World!"
console.log(API_URL); // Outputs "https://demo.com"
```

## Customization

1. Update package name and metadata in `package.json`
2. Modify the source files in the `src` directory
3. Update types in `src/types.ts`
4. Add your SDK functionality in dedicated files and export them in `src/index.ts`

## Testing

Tests are written using Mocha and Chai. The test setup provides:

- Chai assertions with `should` and `expect`
- Sinon for mocks, stubs, and spies
- ProxyQuire for mocking dependencies

Add your tests in the `test` directory with the `.spec.ts` suffix.

## Publishing

```bash
# Build the SDK before publishing
pnpm build

# Publish to npm
npm publish
```

## License

This project is licensed under the ISC License - see the LICENSE file for details.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request