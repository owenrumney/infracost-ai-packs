# infracost-ai-packs

Packs for [Infracost AI](https://github.com/infracost/cli-ai). A pack is data:
YAML and Markdown that name library blocks living in the CLI and supply their
parameters and text. There is no executable code here.

## Use it

```sh
infracost-ai pack registry add github.com/owenrumney/infracost-ai-packs
infracost-ai pack search
infracost-ai pack install owenrumney/tests
```

## What is here

| Pack | What it is for |
| --- | --- |
| `owenrumney/tests` | Run the tests before you commit |

## Layout

`infracost-ai.yaml` at the root lists what this repository offers. Each entry
names a pack id and the directory holding it. The id has to match the id in
that pack's own `pack.yaml`; install refuses a pack that disagrees.

## Check it before pushing

```sh
infracost-ai pack validate .
```

That reads the index and every pack it names, the way install will.
