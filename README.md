# Tor for StartOS, in Kilombino's registry

The official Start9 StartOS package of **Tor** (`tor`, version
`0.4.9.17:1`), offered in [registry.kilombino.com](https://registry.kilombino.com)
so that the optional `tor` dependency of Bitcoin Knots (`bitcoind`
`#knots:29.5.1:2`) can be installed from the same registry.

**Nothing in the software is changed.** These are the `.s9pk` files that Start9
publishes in [Start9Labs/tor-startos](https://github.com/Start9Labs/tor-startos/releases/tag/v0.4.9.17_1)
and lists in the official Start9 registry (registry.start9.com), checked against
the SHA-256 hashes in Start9's release notes and against the merkle commitment
(`rootSighash`) that registry.start9.com publishes for each architecture, and
re-signed with Kilombino's key so StartOS does not ask you to trust another
signer. The only edit is a no-op on the manifest (`packageRepo` set to its
own value, still pointing to Start9's repository); editing it re-signs it.
Needs StartOS 0.4.2 or later. The image installs tor 0.4.9.17 from Alpine's official package, plus the lyrebird and snowflake bridge transports built from the Tor Project's sources at pinned commits.

All credit to the Tor Project ([tpo/core/tor](https://gitlab.torproject.org/tpo/core/tor/)) and to Start9 for the package. Licence: BSD-3-Clause, as upstream.

## Releases

- `v0.4.9.17_1`: x86_64 and aarch64, re-signed from Start9's v0.4.9.17_1.

  | file | upstream SHA-256 | re-signed SHA-256 |
  |---|---|---|
  | `tor_x86_64.s9pk` | `31cebbbea0a2438459470bfb09932391931eca762889548ace2f687e1eadd257` | `80386d1412aea4637014e79d7b90fb66db4fa353a5ea48cc742b1decbef14c2b` |
  | `tor_aarch64.s9pk` | `20207ac75d3e535fe2502efb4f3691c44946e27de7ad17cc317de48fc2bf9a57` | `63d140b11b5b178c58df714e9ce379f8de60858083b0871e1509d7e1756d2e8b` |
