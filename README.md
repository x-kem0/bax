# Bax
terminal backup tool with a borg backend

## usage

Install borg through your package manager

Place `bax` into a place of your choosing and add it to your shell paths
It is recommended to use `$HOME/.local/bin`

Intiialize a borg repo with bax:
```
bax repo init <repokey/unencrypted> <name> <location>
```

Locations may either local to the system, or specified as an ssh location:
```
bax repo init repokey remote ssh://user@host.tld/./backups
```

From there, files and directories are added with `bax add <file/dir>`
```
bax add /home/user/Documents
```

To run the backup, use `bax go`

Because the repos are plain borg repos, restoration can be done using `borg` itself

## All commands

```
bax add
```
Add files or directories to be backed up

```
bax remove
```
Remove files or directories from bax (unimplemented)

```
bax list
```
List all tracked files and directories

```
bax go
```
Perform backup to all configured repositories

```
bax repo list
```
List all configured repositories

```
bax repo init repokey <name> <location>
```
Initialize a repokey borg repository with the given name and location

```
bax repo init repokey <name> <location>
```
Initialize a repokey borg repository with the given name and location

```
bax repo init unencrypted <name> <location>
```
Initialize an unencrypted borg repository with the given name and location

```
bax repo remove <name>
```
Remove a repository from bax (unimplemented)

