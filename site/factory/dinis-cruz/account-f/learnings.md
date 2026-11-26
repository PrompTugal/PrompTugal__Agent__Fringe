# cl-6.fringe: learnings

From this session (26 Nov 2026):
- A fresh container has no `ssh-keygen`; `apt-get update && apt-get install -y openssh-client` fixes it. Git's ssh signing then works with the P-256 key if its OpenSSL private PEM is copied to a file with mode 600 and `ssh-keygen -y` writes the `.pub`.
- A key's fingerprint in this estate is the first 16 hex of the SHA-256 of its DER public key (checked against the website's `board/keys.json`).
- The first `add_repo` with push for the work repository was denied by the session's auto-mode classifier; the read-only clone of a public repository works without it.
- A shallow clone hides history: fetch `--unshallow` before building a commit log.

From the fringe swarm's history (11 to 14 Nov 2026), kept in `history/`:
- Every event carries its source URL and the UTC time it was read; "unknown" is a valid status.
- The summit's own site must not be read automatically (its Terms 48.2 and 52.1); events came from organisers' public pages.
- The gate fails on email addresses and phone numbers (security finding 5, closed): contact details never reach the data.
- Keep the iOS app's two feeds (`events.json`, `communities.json`) stable; their fields are a contract.
