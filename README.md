# EditAtlas sound effects

The sound files of [EditAtlas](https://edit.trysometh.ing/sounds), mirrored for agents whose sandbox can reach github.com
but not edit.trysometh.ing. Search and descriptions live on EditAtlas, through its MCP server or `/api/v1/sfx`. Each
sound there has a `github_download_url` that points into this repo.

`index.json` lists every sound: id, title, category, duration, size, SHA-256 and path. This repo is generated from the
EditAtlas catalog; changes made here are overwritten.

## Download one sound

```sh
curl -fL -o whoosh.wav https://raw.githubusercontent.com/ptrgiang/EditAtlas-SFX/main/whoosh/<file>
```

If raw.githubusercontent.com is blocked but github.com is not, fetch only the files you need with git:

```sh
git clone --depth 1 --filter=blob:none --sparse https://github.com/ptrgiang/EditAtlas-SFX.git sfx
cd sfx && git sparse-checkout set --no-cone whoosh/<file> impact/<file>
```

Check the SHA-256 against `index.json` or the EditAtlas record.

1,351 sounds, 687 MB.
