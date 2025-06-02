<!-- Space: Projects -->
<!-- Parent: TerraformModuleTemplate -->
<!-- Title: Examples TerraformModuleTemplate -->
<!-- Label: Examples -->
<!-- Include: ./../disclaimer.md -->
<!-- Include: ac:toc -->

## Common

```hcl
locals {
  tags = merge(
    var.tags,
    {
      ManagedBy = "terraform"
    }
  )
}

module "main" {
 source = git::https://github.com/hadenlabs/terraform-module-template.git//modules/basic?ref=0.0.0
  module_enabled = var.module_enabled
  stage          = var.stage
  namespace      = var.namespace
  tags           = local.tags
  use_fullname   = var.use_fullname
  name           = var.name
}
```
