# confidential-sglang-ci

Runs [confidential-sglang](https://github.com/confidential-dot-ai/confidential-sglang)'s
`images` workflow, because GitHub Actions are disabled on confidential-sglang
(an sglang fork; enabling them needs a repository admin). The workflow
definition lives in confidential-sglang (`.github/workflows/images.yml`); this
repository only calls it with a source commit.

Images: `ghcr.io/confidential-dot-ai/confidential-sglang/{engine,router}`,
tagged `sha-<commit>`. Release record: release `images-<12 hex>` here, asset
`images-<12 hex>.json` (copied to confidential-sglang's release of the same
name). Once Actions are enabled on confidential-sglang, it runs natively and
writes the release there; archive this repository then.
