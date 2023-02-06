---
title: TiDB Cloud CLI Quick Start
summary: Learn how to manage TiDB Cloud resources through the TiDB Cloud CLI.
---

# TiDB Cloud CLI Quick Start

TiDB Cloud provides a command-line interface (CLI) [`ticloud`](https://github.com/tidbcloud/tidbcloud-cli) for you to interact with TiDB Cloud from your terminal with a few lines of commands. For example, you can easily perform the following operations using `ticloud`:

- Create, delete, and list your clusters.
- Import data from Amazon S3 or local files to your clusters.

## Before you begin

- Have a TiDB Cloud account. If you do not have one, [sign up for a free trial](https://tidbcloud.com/free-trial).
- [Create a TiDB Cloud API Key](https://docs.pingcap.com/tidbcloud/api/v1beta#section/Authentication/API-Key-Management).

## Installation

<SimpleTab>
<div label="macOS/Linux">

For macOS or Linux, you can install `ticloud` using any of the following methods:

- Install via script (recommended)

    ```shell
    curl https://raw.githubusercontent.com/tidbcloud/tidbcloud-cli/main/install.sh | sh
    ```

- Install via [TiUP](https://tiup.io/)

    ```shell
    tiup install cloud
    ```

- Install manually

    Download the pre-compiled binaries from the [releases](https://github.com/tidbcloud/tidbcloud-cli/releases/latest) page and copy them to your desired location for installation.

- Install in GitHub Actions

    To set up `ticloud` in GitHub Action, use [`setup-tidbcloud-cli`](https://github.com/tidbcloud/setup-tidbcloud-cli).

</div>

<div label="Windows">

For Windows, you can install `ticloud` using either of the following methods:

- Install manually

    Download the pre-compiled binaries from the [releases](https://github.com/tidbcloud/tidbcloud-cli/releases/latest) page and copy them to the desired location for installation.

- Install in GitHub Actions

    To set up `ticloud` in GitHub Actions, use [`setup-tidbcloud-cli`](https://github.com/tidbcloud/setup-tidbcloud-cli).

</div>
</SimpleTab>

## Use the TiDB Cloud CLI

View all commands available:

```shell
ticloud --help
```

Verify that you are using the latest version:

```shell
ticloud version
```

If not, update to the latest version:

```shell
ticloud update
```

### Use the TiDB Cloud CLI through TiUP

The TiDB Cloud CLI is also available through [TiUP](https://tiup.io/), with the component name as `cloud`.

View all commands available:

```shell
tiup cloud --help
```

Run commands with `tiup cloud <command>`. For example:

```shell
tiup cloud cluster create
```

Update to the latest version by TiUP:

```shell
tiup update cloud
```

## Quick start

TiDB Cloud [Serverless Tier](/tidb-cloud/select-cluster-tier.md#serverless-tier-beta) (Beta) is the best way to get started with TiDB Cloud. In this section, you will learn how to create a Serverless Tier cluster with TiDB Cloud CLI.

### Create a user profile

Before creating a cluster, you need to create a user profile with your TiDB Cloud API Key:

```shell
ticloud config create
```

> **Warning:**
>
> The profile name **MUST NOT** contain `.`.

### Create a Serverless Tier cluster

To create a Serverless Tier cluster, enter the following command, and then follow the CLI prompts to provide the required information:

```shell
ticloud cluster create
```

## What's next

Check out [CLI reference](/tidb-cloud/cli-reference.md) to explore more features of TiDB Cloud CLI.

## Feedback

If you have any questions or suggestions on the TiDB Cloud CLI, feel free to create an [issue](https://github.com/tidbcloud/tidbcloud-cli/issues/new/choose). Also, we welcome any contributions.