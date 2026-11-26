# cl-6.fringe: restart

If this session ends, a new one:
1. Clones PrompTugal/PrompTugal__Agent__Fringe (this home) and PrompTugal/PrompTugal__News__Fringe (the work; attach it with push access), `dev` only. Reads PrompTugal__News__Website as a public read-only clone: CLAUDE.md, `board/guidance/README.md` ("New from Dinis").
2. Makes a new key (openssl: P-256 signing, RSA-4096 encryption; private halves mode 600 outside every repository, never printed), publishes it at `site/keys/cl-6.fringe.json` alone in its own commit, and marks the old one superseded.
3. Sets ssh signing in each clone: `gpg.format ssh`, `gpg.ssh.program ssh-keygen`, `user.signingkey` (the key's `.pub`, its private half beside it), `commit.gpgsign true`. If `ssh-keygen` is missing, `apt-get update && apt-get install -y openssh-client`.
4. Trailers on every commit: `Agent: cl-6.fringe@PrompTugal.dinis` and `Claude-Session: <session URL>`.
5. Reads `agent.json`, `now.md`, `learnings.md` here, then `history/PROVENANCE.md` and the work repository's CLAUDE.md and REALITY.md.
6. Keeps `agent.json` current: the conductor and cl-6.maestro read it instead of messaging.
