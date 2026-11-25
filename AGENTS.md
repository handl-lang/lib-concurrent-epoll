# lib-concurrent-epoll

Linux epoll scheduler for the `concurrent` step-arrow contract — drives
tasks on fd readiness, timers, channels and locks.

## Layout

| path | role |
| --- | --- |
| `src/index.hnl` | the scheduler module (`concurrent-epoll`) |
| `src/concurrent-epoll.test.hnl` | tests |
| `pkg.hnl` | manifest — deps `concurrent`, `libc`, `curl`, `tls-libssl`, `ws-c`, `math` (`branch:main`) |
| `scripts/hnl-gate.sh` | `.hnl` gate |
| `workflows/gate.yaml` | CI — shared `handl-gates` campaign |

## Contract

- Linux/epoll backend of the `concurrent` contract — the OS-bound
  counterpart of `lib-concurrent-js`.
- Pure `.hnl` over `ffi.call`; no Rust crate.

## Verification

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
