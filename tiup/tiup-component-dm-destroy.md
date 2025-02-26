---
title: tiup dm destroy
summary: The `tiup dm destroy` command stops the cluster, deletes log, deployment, and data directories for each service, and also deletes parent directories created by `tiup-dm`. The syntax is `tiup dm destroy <cluster-name> [flags]`. The option `-h, --help` prints help information. The output is the execution log of tiup-dm.
---

# tiup dm destroy

After an application goes offline, if you want to release the machines occupied by the cluster for use by other applications, you need to clean up the data on the cluster and the deployed binary files. To destroy the cluster, the `tiup dm destroy` command performs the following operations:

- Stops the cluster.
- For each service, delete its log directory, deployment directory, and data directory.
- If the parent directory of the data directory or deployment directory of each service is created by `tiup-dm`, also delete the parent directory.

## Syntax

```shell
tiup dm destroy <cluster-name> [flags]
```

`<cluster-name>`: the name of the cluster to be destroyed.

## Option

### -h, --help

- Prints the help information.
- Data type: `Boolean`
- Default: false

## Output

The execution log of the tiup-dm.
