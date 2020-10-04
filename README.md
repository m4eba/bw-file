## Shell script to download/upload files to a Bitwarden Vault

#### Requirements

- [Bitwarden CLI](https://github.com/bitwarden/cli)
- [jq](https://stedolan.github.io/jq/)
- an active Bitwarden session in the shell

#### Upload

```
$bw-push <remote_folder> <files>
```

Makes secure notes with the filename as name and uploads the file as attachments.
The remote folder needs to exist.
Examples:

```
$bw-push ssh ~/.ssh/id_rsa ~/.ssh/id_rsa.pub
$bw-push ssh ~/.ssh/*id_rsa*
```

#### Download

```
$bw-pull <remote_folder> <regex>
```

Downloads all files matching the regex from a remote folder.
Example

```
$bw-pull ssh ".*id_rsa.*"
```
