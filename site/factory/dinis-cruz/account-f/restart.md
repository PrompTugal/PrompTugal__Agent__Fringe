# cl-6.fringe: restart (archived)

This agent is archived: its history is moved, it has no wake, and the site stays live as it is at https://lisbontechfringe.com (last built 14 Nov 2026, v0.1.1128). Lisbon Tech Fringe was an event site and its team's work ended on 14 Nov 2026.

To pick the section up again, only at Dinis's word, a new session:
1. Clones PrompTugal/PrompTugal__Agent__Fringe (this home) and PrompTugal/PrompTugal__News__Fringe (the work; attached with push access), `dev` only. Reads PrompTugal__News__Website as a public read-only clone: CLAUDE.md, `board/guidance/README.md`.
2. Makes a new key (openssl: P-256 signing, RSA-4096 encryption; private halves mode 600 outside every repository, never printed), publishes it at `site/keys/cl-6.fringe.json` alone in its own commit, and marks the old one superseded.
3. Sets ssh signing in each clone: `gpg.format ssh`, `gpg.ssh.program ssh-keygen`, `user.signingkey`, `commit.gpgsign true`. If `ssh-keygen` is missing: `apt-get update && apt-get install -y openssh-client`.
4. Trailers on every commit: `Agent: cl-6.fringe@PrompTugal.dinis` and `Claude-Session: <session URL>`.
5. Reads `agent.json`, `now.md`, `learnings.md`, then `history/PROVENANCE.md`, the work repository's CLAUDE.md and REALITY.md, and the open notes in `agent.json` (the CNAME finding S2).
6. Asks Dinis what the section covers before doing anything: the site's data (179 events, 11 to 14 Nov 2026) is a record, and `history/PrompTugal__News__Fringe/work/drafts/closing-state.md` has the closing options.
