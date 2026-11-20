# lib-concurrent-epoll

Linux epoll scheduler for the `concurrent` step-arrow contract — drives tasks on fd readiness, timers, channels and locks.

## Layout

```text
src/                     the .hnl sources
pkg.hnl                  package manifest
scripts/hnl-gate.sh      the gate
ci.sh                    bupha entry
```

## Gate

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.
