# aircraft-size-comparison

Relative-size data for seven classes of business aircraft, from turboprop to ultra long-range, as a single JSON file. It belongs to the brand assets and investor material layer of the Oneways repositories. Status: active; not deployed — `scales.json` is the whole repository, and a consumer reads it as a file.

The images the data describes are not in this repository.

## Where it sits

- **Depends on:** nothing.
- **Used by:** no code in this repository, and no published package depends on it.
- **External services:** none.
- **Deployed as:** not deployed.

## Prerequisites

Any JSON parser. There is no build, no package manager, no dependency and no code.

## Setup

```sh
git clone https://github.com/Oneways-AI/aircraft-size-comparison.git
cd aircraft-size-comparison
```

## Run, test, build

| Task | Command |
|---|---|
| Check that the data parses | `python3 -m json.tool scales.json > /dev/null` |

Green is no output and exit status 0. Any JSON parser does the same job.

There is no CI workflow in this repository, and GitHub Actions is switched off for the organisation, so run the check locally before opening a pull request.

## Configuration

None. There is no code, so no environment variable is read and there is no `.env.example`.

## Deploy

Not deployed.

## Repository map

```
scales.json   the data: a reference aircraft, seven entries, and the shared render style
README.md     this file
```

## The data

`scales.json` has three top-level keys.

- `reference` — a sentence naming the aircraft that is treated as 100%.
- `aircraft` — seven objects, one per class, each with `class` (the class name), `model` (the specific type), `scale_pct` (overall length as a percentage of the reference) and `file` (the filename of the render for that class, which this repository does not contain).
- `style` — the render style the set was produced to: `paint`, `lighting`, `ground`, `gear`, `markings`. Every image in the set shares it, which is what makes side-by-side comparison meaningful. The images are synthetic, generated with an image model rather than photographed, and `markings: "none"` records that no registration, livery, logo or legible text appears in any of them.

Read it as data, not as a table to copy: there is exactly one copy of these numbers and it is the file.

**Verify the percentages before relying on them.** `scales.json` carries no aircraft lengths, so nothing in the file lets a reader check its own arithmetic. Checked against published overall lengths for the seven types, the six non-reference percentages are self-consistent against a reference length of about 111 ft, while the `reference` field names an aircraft whose published length is about 99.8 ft. The two do not agree, and on the named reference each of the other six comes out about 10% low. Recompute from published lengths for the types you need.

## Ownership and support

Code owners: see [`.github/CODEOWNERS`](.github/CODEOWNERS). Questions and bug reports go to this repository's issues.

## Further reading

- [`CONTRIBUTING.md`](CONTRIBUTING.md): branches, commits and pull requests
- [`SECURITY.md`](SECURITY.md): how to report a vulnerability
