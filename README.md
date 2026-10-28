# lib-concurrent-epoll

Linux epoll scheduler for the `concurrent` step-arrow contract — drives tasks on fd readiness, timers, channels and locks.

Part of the `handl-lang` org split (ADR-0128). History is a `git subtree
split` of the platform monorepo's `concurrent-epoll/` (via `web`).

## Layout

```text
src/        the .hnl sources
pkg.hnl     dependencies, when any: `{ deps: { <name>: "branch:<ref>" } }`
```

## Gate

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.
