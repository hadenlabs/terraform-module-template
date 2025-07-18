<!-- Space: Projects -->
<!-- Parent: TerraformModuleTemplate -->
<!-- Title: Commands TerraformModuleTemplate -->
<!-- Label: TerraformModuleTemplate -->
<!-- Label: Project -->
<!-- Label: Commands -->
<!-- Include: disclaimer.md -->
<!-- Include: ac:toc -->

# Commands

## Poetry

## Taskfile

### Confluence

#### Sync Markdown with confluence

```{.bash}
task confluence:sync:all
```

### Python

#### Format syntax code python with [black](https://github.com/psf/black)

```{.bash}
task python:fmt -- {{file_name or path}}
```

### Diagrams

#### Publish diagrams

```{.bash}
task diagrams:publish
```

### Mkdocs

#### Generate Website

```{.bash}
task docs:build
```

### Changelog

#### Generate Changelog Next Tag

```{.bash}
task changelog:next APP_TAG={{tag name}}
```

#### Parameters

| Name     | Description   | sample | Required |
| -------- | ------------- | ------ | :------: |
| tag name | Name next tag | 0.1.0  |   yes    |

### Version

#### Version Major

```{.bash}
task version:major
```

#### Version Minor

```{.bash}
task version:minor
```

#### Version Patch

```{.bash}
task version:patch
```

## Infrastructure

### Terragrunt

| Field |        Description        |
| ----- | :-----------------------: |
| STAGE | stage or name environment |

```bash
task terragrunt:init STAGE=core
```

```bash
task terragrunt:apply STAGE=core
```

```bash
task terragrunt:plan STAGE=core
```

```bash
task terragrunt:destroy STAGE=core
```

#### Import

| Field   |           Description           |
| ------- | :-----------------------------: |
| REGION  |          region of aws          |
| STAGE   |    stage or name environment    |
| COMMAND | command for execute with import |

```bash
task terragrunt:import REGION=us-east-1 STAGE=core COMMAND=module.repository_learn_go.github_repository.this learn-go
```

**example**

```bash
task terragrunt:import REGION=us-east-1 STAGE=core COMMAND=module.repository_learn_go.github_repository.this learn-go
```

#### Module

| Field  |        Description        |
| ------ | :-----------------------: |
| REGION |       region of aws       |
| STAGE  | stage or name environment |
| MODULE |  module name to destroy   |

```bash
task terragrunt:module:destroy REGION=us-east-1 STAGE=core MODULE=repository_eslint_config
```

#### State

| Field   |          Description           |
| ------- | :----------------------------: |
| REGION  |         region of aws          |
| STAGE   |   stage or name environment    |
| COMMAND | command for execute with state |

```bash
task terragrunt:state REGION=us-east-1 STAGE=core COMMAND=list
```

### Terraform

#### generate docs terraform for stage

| Field |        Description        |
| ----- | :-----------------------: |
| STAGE | stage or name environment |

```bash
task terraform:docs STAGE=core
```

### Python

#### Format syntax code python with [black](https://github.com/psf/black)

```{.bash}
task python:fmt -- {{file_name or path}}
```

### Diagrams

#### Publish diagrams

```{.bash}
task diagrams:publish
```

### Changelog

#### Generate Changelog Next Tag

```{.bash}
task changelog:next APP_TAG={{tag name}}
```

#### Parameters

| Name     | Description   | sample | Required |
| -------- | ------------- | ------ | :------: |
| tag name | Name next tag | 0.1.0  |   yes    |

### Version

#### Version Major

```{.bash}
task version:major
```

#### Version Minor

```{.bash}
task version:minor
```

#### Version Patch

```{.bash}
task version:patch
```

### Docs

#### build

```{.bash}
task docs:build
```

#### server

```{.bash}
task docs:serve
```
