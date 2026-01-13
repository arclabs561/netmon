# netmon

Passive local-network host tracking (packet sniffing). Emits events when hosts appear/disappear or change behavior (ports, scans, etc.).

## Example

```bash
sudo -E netmon --only log
```

Trigger a command on an event:

```toml
[triggers]
  [triggers.new-host]
    onEvents = ["host.new"]
    doShell = "echo 'new host {{.Host.MAC}} on {{.Host.IPv4}}'"
```

## License

Dual-licensed under MIT or the UNLICENSE.
