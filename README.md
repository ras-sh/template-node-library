# @ras-sh/template-node-library

📦 Node.js library template with TypeScript, testing setup, and modern build tooling.

## Features

- **TypeScript** - Full type safety with modern TS features
- **[tsup](https://tsup.egoist.dev/)** - Fast, zero-config bundler powered by esbuild
- **[Vitest](https://vitest.dev/)** - Fast unit testing with coverage reports
- **[tsx](https://tsx.is/)** - Fast TypeScript execution for development

## Quick Start

```bash
pnpm install
pnpm dev
```

## Building Your Library

1. Add library code in `src/`
2. Add tests in `tests/`
3. Update `package.json` metadata (name, description, keywords, repository)

## Scripts

| Command | Description |
|---------|-------------|
| `pnpm dev` | Run with tsx in watch mode |
| `pnpm build` | Build library with tsup |
| `pnpm test` | Run tests with vitest |
| `pnpm test:coverage` | Run tests with coverage report |
| `pnpm check-types` | Run TypeScript type checking |
| `pnpm check` | Run linter checks |
| `pnpm fix` | Auto-fix linting issues |
| `pnpm changeset` | Create a new changeset |
| `pnpm version` | Update versions based on changesets |
| `pnpm release` | Build and publish to npm |

## Project Structure

```
src/
├── index.ts        # Main entry point
tests/
├── index.test.ts   # Test files
```

## Publishing

This template uses [Changesets](https://github.com/changesets/changesets) for version management and publishing.

### Release Workflow

1. **Create a changeset** when you make changes:
   ```bash
   pnpm changeset
   ```
   Follow the prompts to describe your changes (patch, minor, or major).

2. **Version packages** to update `package.json` and generate changelog:
   ```bash
   pnpm version
   ```

3. **Commit the changes**:
   ```bash
   git add .
   git commit -m "chore: version packages"
   ```

4. **Publish to npm**:
   ```bash
   pnpm release
   ```
   This will build and publish your package to npm.

## License

MIT License - see the [LICENSE](LICENSE) file for details.
