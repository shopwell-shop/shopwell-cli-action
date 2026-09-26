# Shopwell repository rules

This repository is the independently maintained Shopwell CLI setup Action.

- Preserve UTF-8 and existing user changes.
- Shopwell-owned code and `package.json` use the Apache License 2.0 (`Apache-2.0`); root `LICENSE` contains the standard text.
- Preserve every upstream legal text verbatim in root `NOTICE`; never brand or paraphrase its contents.
- Outside `NOTICE`, do not reintroduce Shopware branding, package names, repositories, binaries, or Actions.
- This Action may download binaries only from the independently maintained `shopwell-shop/shopwell-cli` release repository.
- Do not merge or cherry-pick upstream history, copy upstream tags, or force-push.
- Before commit, push, release, or sync completion, run `../sync-upstream/bin/syncctl audit-license shopware-cli-action` and `../sync-upstream/bin/syncctl audit-upstream-dependencies shopware-cli-action`. A failed audit blocks completion.
