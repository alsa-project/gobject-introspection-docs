# ALSA GObject Introspection team

2022/07/11

Takashi Sakamoto

## Introduction

ALSA GObject Introspection team maintains libraries and applications to interact with Linux kernel
for hardware features to process audio and music data.
[GObject Introspection](https://gi.readthedocs.io/) is utilized to provide language bindings for
the libraries.

## Libraries

The team provides some libraries written by C language for system call for Linux sound subsystem.
The libraries utilize [event loop mechanism](https://docs.gtk.org/glib/main-loop.html) in
[GLib](https://docs.gtk.org/glib/), and support
[type/object system](https://docs.gtk.org/gobject/concepts.html) in
[GObject](https://docs.gtk.org/gobject/). Additionally, the libraries also support
[GObject Introspection](https://gi.readthedocs.io/) to provide metadata of public API for
language bindings such as Python 3 module by [PyGObject project](pygobject.readthedocs.io/) and
[gir tool](https://gtk-rs.org/gir/book/) by [gtk-rs project](https://gtk-rs.org/).

### alsactl library

* Operate ALSA Control character device for control functions in Linux sound subsystem.
* Provide `ALSACtl-0.0` namespace.
* documentation: [gobject-introspection-docs/alsactl](https://alsa-project.github.io/gobject-introspection-docs/alsactl/)
* repository: [alsa-gobject](https://github.com/alsa-project/alsa-gobject)

### alsahwdep library

* Operate ALSA HwDep character device for hwdep functions in Linux sound subsystem.
* Provide `ALSAHwdep-0.0` namespace.
* documentation: [gobject-introspection-docs/alsahwdep](https://alsa-project.github.io/gobject-introspection-docs/alsahwdep/)
* repository: [alsa-gobject](https://github.com/alsa-project/alsa-gobject)

### alsarawmidi library

* Operate ALSA Rawmidi character device for rawmidi functions in Linux sound subsystem.
* Provide `ALSARawmidi-0.0` namespace.
* documentation: [gobject-introspection-docs/alsarawmidi](https://alsa-project.github.io/gobject-introspection-docs/alsarawmidi/)
* repository: [alsa-gobject](https://github.com/alsa-project/alsa-gobject)

### alsatimer library

* Operate ALSA Timer character device for timer functions in Linux sound subsystem.
* Provide `ALSATimer-0.0` namespace.
* documentation: [gobject-introspection-docs/alsatimer](https://alsa-project.github.io/gobject-introspection-docs/alsatimer/)
* repository: [alsa-gobject](https://github.com/alsa-project/alsa-gobject)

### alsaseq library

* Operate ALSA Sequencer character device for sequencer functions in Linux sound subsystem.
* Provide `ALSASeq-0.0` namespace.
* documentation: [gobject-introspection-docs/alsaseq](https://alsa-project.github.io/gobject-introspection-docs/alsaseq/)
* repository: [alsa-gobject](https://github.com/alsa-project/alsa-gobject)

### hitaki library

* operate ALSA HwDep character device for model specific functionalities supported by drivers
  in ALSA firewire stack.
* Provide `Hitaki-0.0` namespace.
* documentation: [gobject-introspection-docs/hitaki](https://alsa-project.github.io/gobject-introspection-docs/hitaki/)
* repository: [libhitaki](https://github.com/alsa-project/libhitaki)

### hinawa library

* Operate Linux FireWire character device for asynchronous packet and topology generation in
  IEEE 1394 bus.
* Provide `Hinawa-3.0` namespace.
* documentation: [gobject-introspection-docs/hinawa](https://alsa-project.github.io/gobject-introspection-docs/hinawa/)
* repository: [libhinawa](https://github.com/alsa-project/libhinawa)

### hinoko library

* Operate Linux FireWire character device for isochronous packet and resources in IEEE 1394 bus.
* Provide `Hinoko-0.0` namespace.
* documentation: [gobject-introspection-docs/hinoko](https://alsa-project.github.io/gobject-introspection-docs/hinoko/)
* repository: [libhinoko](https://github.com/takaswie/libhinoko)

## Rust crates

The team maintains crates automatically generated by [gir tool](https://gtk-rs.org/gir/book/) provided
by [gtk-rs project](https://gtk-rs.org/) with gir files provided by the C language libraries.

### alsactl/alsactl-sys crates

* API and FFI crates for alsactl library.
* crates.io: [alsactl](https://crates.io/crates/alsactl), [alsactl-sys](https://crates.io/crates/alsactl)
* documentation: [alsactl](https://docs.rs/alsactl/), [alsactl-sys](https://docs.rs/alsactl-sys/)
* repository: [alsa-gobject-rs](https://github.com/alsa-project/alsa-gobject-rs)

### alsahwdep/alsahwdep-sys crates

* API and FFI crates for alsahwdep library.
* crates.io: [alsahwdep](https://crates.io/crates/alsahwdep), [alsahwdep-sys](https://crates.io/crates/alsahwdep-sys)
* documentation: [alsahwdep](https://docs.rs/alsahwdep/), [alsahwdep-sys](https://docs.rs/alsahwdep-sys/)
* repository: [alsa-gobject-rs](https://github.com/alsa-project/alsa-gobject-rs)

### alsarawmidi/alsarawmidi-sys crates

* API and FFI crates for alsarawmidi library.
* crates.io: [alsarawmidi](https://crates.io/crates/alsarawmidi), [alsarawmidi-sys](https://crates.io/crates/alsarawmidi-sys)
* documentation: [alsarawmidi](https://docs.rs/alsarawmidi/), [alsarawmidi-sys](https://docs.rs/alsarawmidi-sys/)
* repository: [alsa-gobject-rs](https://github.com/alsa-project/alsa-gobject-rs)

### alsatimer/alsatimer-sys crates

* API and FFI crates for alsatimer library.
* crates.io: [alsatimer](https://crates.io/crates/alsatimer), [alsatimer-sys](https://crates.io/crates/alsatimer-sys)
* documentation: [alsatimer](https://docs.rs/alsatimer/), [alsatimer-sys](https://docs.rs/alsatimer-sys/)
* repository: [alsa-gobject-rs](https://github.com/alsa-project/alsa-gobject-rs)

### alsaseq/alsaseq-sys crates

* API and FFI crates for alsaseq library.
* crates.io: [alsaseq](https://crates.io/crates/alsaseq), [alsaseq-sys](https://crates.io/crates/alsaseq-sys)
* documentation: [alsaseq](https://docs.rs/alsaseq/), [alsaseq-sys](https://docs.rs/alsaseq-sys/)
* repository: [alsa-gobject-rs](https://github.com/alsa-project/alsa-gobject-rs)

### hitaki/hitaki-sys crates

* API and FFI crates for hitaki library.
* crates.io: [hitaki](https://crates.io/crates/hitaki), [hitaki-sys](https://crates.io/crates/hitaki-sys)
* documentation: [hitaki](https://docs.rs/hitaki/), [hitaki-sys](https://docs.rs/hitaki-sys/)
* repository: [hitaki-rs](https://github.com/alsa-project/hitaki-rs)

### hinawa/hinawa-sys crates

* API and FFI crates for hinawa library.
* crates.io: [hinawa](https://crates.io/crates/hinawa), [hinawa-sys](https://crates.io/crates/hinawa-sys)
* documentation: [hinawa](https://docs.rs/hinawa/), [hinawa-sys](https://docs.rs/hinawa-sys/)
* repository: [hinawa-rs](https://github.com/alsa-project/hinawa-rs)

### hinoko/hinoko-sys crates

* API and FFI crates for hinoko library.
* crates.io: [hinoko](https://crates.io/crates/hinoko), [hinoko-sys](https://crates.io/crates/hinoko-sys)
* documentation: [hinoko](https://docs.rs/hinoko/), [hinoko-sys](https://docs.rs/hinoko-sys/)
* repository: [hinoko-rs](https://github.com/takaswie/hinoko-rs)

## Applications

At present the team maintains some service programs to operate audio and music units
in IEEE 1394 bus supported by ALSA firewire stack for their model specific functionalities.

### snd-bebob-ctl-service

* Maintain control elements for devices to which ALSA `bebob` driver is bound for BrigdeCo. Enhanced
  BreakOut Box (BeBoB) ASICs and firmware.
* implementation of protocol: `bebob-protocols` crate
* repository: [snd-firewire-ctl-services](https://github.com/alsa-project/snd-firewire-ctl-services/)

### snd-fireworks-ctl-service

* Maintain control elements for devices to which ALSA `fireworks` driver is bound for Echo Audio
  Fireworks board module.
* implementation of protocol: `efw-protocols `crate
* repository: [snd-firewire-ctl-services](https://github.com/alsa-project/snd-firewire-ctl-services/)

### snd-oxfw-ctl-service

* Maintain control elements for devices to which ALSA `oxfw` driver is bound for Oxford Semiconductor
  FW970/971 ASICs and firmware.
* implementation of protocol: `oxfw-protocols `crate
* repository: [snd-firewire-ctl-services](https://github.com/alsa-project/snd-firewire-ctl-services/)

### snd-dice-ctl-service

* Maintain control elements for devices to which ALSA `dice` driver is bound for TC Applied
  Technologies (TCAT) Digital Interface Communication Engine (DICE) ASICs and firmware.
* implementation of protocol: `dice-protocols` crate
* repository: [snd-firewire-ctl-services](https://github.com/alsa-project/snd-firewire-ctl-services/)

### snd-firewire-digi00x-ctl-service

* Maintain control elements for devices to which ALSA `firewire-digi00x` driver is bound for AVID
  Digidesign Digi 00x family.
* implementation of protocol: `dg00x-protocols` crate
* repository: [snd-firewire-ctl-services](https://github.com/alsa-project/snd-firewire-ctl-services/)

### snd-firewire-tascam-ctl-service

* Maintain control elements for devices to which ALSA `firewire-tascam` driver is bound for TASCAM
  FireWire series.
* implementation of protocol: `tascam-protocols` crate
* repository: [snd-firewire-ctl-services](https://github.com/alsa-project/snd-firewire-ctl-services/)

### snd-fireface-ctl-service

* Maintain control elements for devices to which ALSA `fireface` driver is bound for RME Fireface
  series.
* implementation of protocol: `ff-protocols` crate
* repository: [snd-firewire-ctl-services](https://github.com/alsa-project/snd-firewire-ctl-services/)

### snd-firewire-motu-ctl-service

* Maintain control elements for devices to which ALSA `firewire-motu` driver is bound for Mark of
  the Unicorn (MOTU) FireWire series.
* implementation of protocol: `motu-protocols` crate
* repository: [snd-firewire-ctl-services](https://github.com/alsa-project/snd-firewire-ctl-services/)

## Support

* Please file issues into each github repository if finding them.
* Post messages to [alsa-devel mailing list](https://mailman.alsa-project.org/mailman/listinfo/alsa-devel)
* It's not preferable to contact to indivisual developers directly.
