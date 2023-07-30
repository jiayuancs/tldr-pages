# alias [modified]

> Creates aliases -- words that are replaced by a command string.
> Aliases expire with the current shell session unless defined in the shell's configuration file, e.g. `~/.bashrc`.
> More information: <https://tldp.org/LDP/abs/html/aliases.html>.

- List all aliases:

`alias`

- Create a generic alias:

`alias {{la}}='{{ls -A}}'`

- View the command associated to a given alias:

`alias {{la}}`

- Remove an aliased command:

`unalias {{la}}`
