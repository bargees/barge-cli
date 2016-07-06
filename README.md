# Barge-CLI

SSH helper for Vagrant to execute ssh much faster than `vagrant ssh`

## Usage: barge `[vm-name]` `[command]`

- `[vm-name]` is defined at `config.vm.define` line in Vagrantfile.  
If it's omitted, it will use SSH config for the first VM in Vagrantfile.

- If `[command]` is omitted, you will login to the VM instead of executing a command.

## Equivalent commands

### To login a VM,

```bash
$ vagrant ssh
$ barge
```

### Execute a command through SSH

```bash
$ vagrant ssh -c "docker version"
$ barge docker version
```

### If Vagrantfile has multiple VMs,

```bash
$ vagrant ssh node-01 -c "docker version"
$ barge docker version
```

```bash
$ vagrant ssh node-02 -c "docker version"
$ barge node-02 docker version
```
