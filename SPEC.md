# clusterform

## Overview

A set of modules and user interfaces (initially a CLI) that can provision CoreOS clusters according to a set of decisions made by the user.


## User Input

The user can make the following decisions about the cluster to be created.

### Infrastructure

e.g. VirtualBox/Vagrant, AWS, DigitalOcean, GCE, bare metal.

### Host Type

Captures the information needed to choose a machine type for a given cloud provider. e.g. "m1-large" for AWS. Will probably be however Terraform refers to these things.

### Groups

Named groups of machines, something like an environment. Each group has a name, a list of (host type, list of metadata keypairs) pairs.

### Etcd Topology

Choose from a list of topologies as per https://github.com/coreos/etcd/blob/master/Documentation/clustering.md.

## Cluster Creation

The cluster is created with Terraform.
