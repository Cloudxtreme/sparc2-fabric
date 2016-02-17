SPARC Fabric Script (sparc2-fabric)
================

## Description

Fabric script for managing a SPARC instance.

## Installation

Follow directions at http://www.fabfile.org/installing.html to install fabric.  On Ubuntu you can most easily run, `sudo apt-get install fabric`.

Create a `instances.py` file in the same directory as the `fabfile.py`.  `instances.py` is in `.gitignore` so will not be committed.  This file includes connection and other information, so that fab commands are streamlined.

```javascript
INSTANCES = {
    "dev": {
        "ident":  "~/workspaces/public/sparc2-ansible.git/.vagrant/machines/default/virtualbox/private_key",
        "host": "localhost",
        "user": "vagrant"
    },
    "prod": {
        "ident":  "~/auth/keys/sparc-1.pem",
        "host": "sparc.wfp.org",
        "user": "ubuntu"
    }
}
```

## Usage

Cd into the main directory with the `fabfile.py`.  When you call fab, start with `sparc:instancehost` so that the host and identity key are loaded automatically from `instances.py`.

To see a list of tasks run:

```
fab -l
```

To see the long description of a task run:

```
fab -d taskname
```

A few examples:

```
```

## Contributing

We are currently accepting pull requests for this repository. Please provide a human-readable description with a pull request and update the README.md file as needed.
