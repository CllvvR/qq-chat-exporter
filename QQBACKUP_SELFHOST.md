# QQBackup self-hosted source baseline

This fork preserves QQ Chat Exporter for a self-hosted QQBackup installation.
The `qqbackup-selfhost` branch is pinned to upstream commit
`7d154b847a0cb3f9cffbdb126598c4d1434995ba`; upstream updates are reviewed manually.

The running API launcher and Rust bridge were checked against this source
baseline. An exact reproducible source revision for the prebuilt Rust binary
has not been established. Keep the known-working receiver image as the
restoration artifact; a source rebuild still needs isolated API validation.

QQBackup uses its own local web UI and authenticated loopback interfaces.
NapCat's personal rkey/signing/proxy dependencies are removed in the companion
private maintenance repository: https://github.com/CllvvR/NapCatQQ-selfhost .
The public NapCat fork preserves the unmodified upstream baseline.
QQBackup controls QCE startup through its on-demand adapter, and keeps QQ
login data, messages, configuration and credentials outside both repositories.

Keep a complete Git bundle, the receiver image, the runtime source overlay,
and the required QQ/NapCat packages on the NAS. Do not use `latest` when
rebuilding a known deployment. Preserve upstream GPL-3.0 license notices.
