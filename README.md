[![CloudNativePG](./logo/cloudnativepg.png)](https://cloudnative-pg.io/)

# CloudNativePG API

Go types for the [CloudNativePG](https://github.com/cloudnative-pg/cloudnative-pg)
custom resources (`Cluster`, `Backup`, `ScheduledBackup`, `Pooler`,
`Database`, `Publication`, `Subscription`, image catalogs, and others), API
group `postgresql.cnpg.io/v1`.

Import it to read or write CloudNativePG resources from your own Go code, such
as a controller, a tool, or a test, without depending on the whole operator:

```go
import apiv1 "github.com/cloudnative-pg/api/pkg/api/v1"
```

## Relation with the operator repository

This repository is a read-only mirror. The source of truth is the `api/`
directory of the
[cloudnative-pg/cloudnative-pg](https://github.com/cloudnative-pg/cloudnative-pg)
repository.

- Every push to `main` in the operator repository triggers a sync that
  updates this repository.
- Tags are propagated only for the `.0` release of each minor version and its
  release candidates, because only those are cut from `main`. Patch releases
  come from release branches, whose API may differ from `main`.

Do not open pull requests with API changes here. Send them to the operator
repository, they are synced back automatically.
