---
layout: "bitbucket"
page_title: "Bitbucket: bitbucket_deployment_variable"
sidebar_current: "docs-bitbucket-resource-deployment-variable"
description: |-
  Manage variables for your pipelines deployment environments
---


# bitbucket\_deployment\_variable

This resource allows you to configure deployment variables.

# Example Usage

```hcl
resource "bitbucket_deployment_variable" "country" {
  deployment = "terraform-code"
  owner      = "myteam"
  name = "COUNTRY"
  value = "Kenya"
  secured = false
}
```

# Argument Reference

* `deployment` - (Required) The deployment ID you want to assign this variable to.
* `name` - (Required) The name of the variable
* `value` - (Required) The stage (Test, Staging, Production)
* `secured` - (Optional) Boolean indicating whether the variable contains sensitive data
* `uuid` - (Computed) The UUID of the variable
