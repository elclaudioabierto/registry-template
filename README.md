# AgentKit Registry Template

Use this template to bootstrap a custom AgentKit registry.

## Files

- `index.yaml`: top-level registry index consumed by `@agentkit/core`
- `recipes/*.yaml`: recipe definitions validated by `@agentkit/schema`

## Local testing

1. Create a source config in your project:

```yaml
version: "1"
sources:
  - id: local
    type: local
    path: ./templates/registry-template
    priority: 1
```

2. Run CLI commands:

```bash
pnpm build
pnpm agentkit -- list recipes --json
pnpm agentkit -- inspect my-recipe
```

## Docs

Main documentation is in `apps/docs`. Merge long-form usage guides there as the scaffold evolves.

## TODO

- Add source-specific auth for private GitHub raw registries
- Add recipe linting command
- Add scaffold command that copies this template into a target directory
