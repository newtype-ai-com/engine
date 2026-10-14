# Newtype engine modules

Signed, prebuilt binaries of the Newtype engine modules. This repository holds
releases only; the source is not published here.

| Module | Decides | Contract |
|---|---|---|
| `nt-judge` | whether an autonomous agent may let its model judge a shell command, or must ask a person | `judge.v1` |
| `nt-grant` (planned) | delegation-chain validity and execution-grant decisions | `grant.v1` |
| `nt-session-proof` (planned) | DPoP session proof: sign (client), verify (server) | `session-proof.v1` |
| `nt-passkey` (planned) | WebAuthn registration and assertion verification | `passkey.v1` |
| `nt-origin` (planned) | turn origin and subagent spawn provenance | `origin.v1` |

Every module is stateless: one versioned JSON request in, one JSON response
out. An unknown contract version is an error, never a default allow.

## Verifying a download

Each release lists `SHA256SUMS` and its signature. Check the hash before
use; consumers pin a version and hash.

```sh
shasum -a 256 -c SHA256SUMS --ignore-missing
```

The open-source Nexus server is at https://github.com/newtype-ai-com/nexus
(Apache-2.0, `gopkg.in/newtype-ai-com/nexus.v0`).

## Licence

The binaries are proprietary; see [LICENSE](LICENSE).
