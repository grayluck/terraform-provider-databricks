---
subcategory: "Workspace"
---
# databricks_directory Data Source

-> **Note** If you have a fully automated setup with workspaces created by [databricks_mws_workspaces](../resources/mws_workspaces.md) or [azurerm_databricks_workspace](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/databricks_workspace), please make sure to add [depends_on attribute](../index.md#data-resources-and-authentication-is-not-configured-errors) in order to prevent _authentication is not configured for provider_ errors.

This data source allows to get information about a directory in a Databricks Workspace.

## Example Usage

```hcl
data "databricks_notebook" "prod" {
  path = "/Production"
}
```

## Argument Reference

* `path` - (Required) Path to a directory in the workspace

## Attribute Reference

This data source exports the following attributes:

* `object_id` - directory object ID
