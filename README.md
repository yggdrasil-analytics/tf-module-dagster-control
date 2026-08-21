# tf-module-dagster-control

Terraform module that deploys the Dagster control plane: the webserver (UI and GraphQL API) and the daemon (schedules, sensors, and the run queue).

Code locations connect to this plane rather than running their own webserver and daemon.

This is a reusable module. Another Terraform project calls it and supplies the inputs.

## Usage

```hcl
module "dagster_control" {
  source = "git::https://github.com/yggdrasil-analytics/tf-module-dagster-control.git"
}
```

Pin the source with `?ref=<tag>` so callers get a fixed version rather than whatever is on `main`.
