# Configuration and CLI Reference

This folder contains device-specific verification commands and configuration guidance for the Packet Tracer simulation.

## Device command reference

See [Device Verification Commands](Device-Verification-Commands.md) for CLI targets and command groups covering:

- India Head Office multilayer switches and routers
- WAN aggregation multilayer switch
- India branch router, ASA and MLS
- Madrid edge router, ASA and MLS
- Head Office ASA firewalls and NOC access switch

## Safe use

- The command blocks are primarily verification commands, not a replacement configuration.
- Run a command on the exact device named in the section.
- Confirm Packet Tracer model support; IOS and ASA command syntax differs.
- Save a backup before changing a working device.
- Never paste a configuration from a different device or interface without checking the current running configuration.
