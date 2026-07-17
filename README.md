# ext-sourcer

Public extension-definition repository for **Sourcer** (sourcer.express) — the
AI sourcing agent for hard-to-find products and services. Owns and publishes
`@sneat/extension-sourcer-contract`; the paired implementation repo is
[`sourcer`](https://github.com/sneat-co/sourcer), which consumes the published
package and owns the runtime/app code.

## Layout

```text
typespec/   # frozen wire contract
backend/    # contract-facing Go definitions and checks
frontend/   # @sneat/extension-sourcer-contract workspace
```

## Publishing

Push to `main` touching `frontend/**` publishes via the shared
`sneat-co/cicd` npm-publish workflow (`.github/workflows/publish.yml`),
or run the workflow manually with a version specifier.

Spec & architecture: `sneat-co/backstage` — `spec/features/sourcer/`,
`docs/architecture/sourcer.md`.
