These files provide an Arch Linux example for running the iKey 2032 with
OpenCT and PC/SC. OpenCT must be built with USB and PC/SC support and install
`openct-control` and `ifdhandler` to `/usr/bin`.

| File | Destination |
| --- | --- |
| `watch-ikey2k` | `/usr/lib/openct/watch-ikey2k` (executable) |
| `openct-ikey2k.service` | `/usr/lib/systemd/system/openct-ikey2k.service` |
| `openct-ikey2k.conf` | `/etc/reader.conf.d/openct-ikey2k.conf` |
| `pcscd-openct.conf` | `/usr/lib/systemd/system/pcscd.service.d/openct.conf` |

Enable the OpenCT service and restart PC/SC after installing these files.
Allow five seconds for a newly connected iKey to settle. The monitor then
starts its handler and asks PC/SC to rescan the configured channels.
