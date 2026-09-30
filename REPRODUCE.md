# Reproduce on a fresh subject, sequentially

Obtain conformance/evidence-sufficiency-v1/, conformance/evidence-sufficiency-v1.1/ and conformance/evidence-sufficiency-v1.2/ at REMORA c1345b1f9e0f877454bf996b2160d533c5a9b16a. Copy adapter/ and manifests/ contents to that fresh subject root. Check every file against RUN-PLAN-FROZEN.json source_files before and after execution.

Use CA 0.7.0 at 5fa2ff587497b00ac684a767335b9068f7e520a6 and Python 3.14.3. For each row listed in the frozen plan, sequentially:

```sh
python3 -B /path/to/pinned-ca/corpus_adequacy.py /path/to/fresh-subject/ca_known-row1-verdict.manifest.json --json > new-row1.json
```

Repeat with the other five manifest names. Never run concurrent mutations on a shared subject. Exit 1 can mean a completed measurement with survivors; inspect controls and failures. Neither the upstream --check snapshot identity nor source hash is a projected outcome. Trusted-local does not provide network isolation; the measured sources/adapters make no network calls. Do not overwrite retained originals.
