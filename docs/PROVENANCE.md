# Provenance ledger — Vaani

Append-only. Every third-party thing this project runs, vendors or depends on gets a row here
**before it is ever run** — source, licence, version, who audited it and when, and what it is
permitted to touch.

This is Principle 12, blast radius before capability, written as a table. A dependency you have
not audited is a capability you have granted without deciding to.

This course runs nothing but `granth.py` and the Python standard library. The table stays, so
that the day something is added, there is a place for it.

| What | Source | Version | Licence | Audited on | Audited by | Permitted scope |
| ---- | ------ | ------- | ------- | ---------- | ---------- | --------------- |
