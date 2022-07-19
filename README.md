ALSA GObject Introspection team maintains libraries and applications to interact with Linux kernel
for hardware features to process audio and music data.
[GObject Introspection](https://gi.readthedocs.io/) is utilized to provide language bindings for
the libraries.

## Libraries

The team provides libraries written by C language to execute system calls for Linux sound
subsystem as well as Linux FireWire subsystem for reasons. The libraries support
[type/object system](https://docs.gtk.org/gobject/concepts.html) in
[GLib](https://docs.gtk.org/glib/)/[GObject](https://docs.gtk.org/gobject/), as well as
[event loop mechanism](https://docs.gtk.org/glib/main-loop.html) in
[GLib](https://docs.gtk.org/glib/). The libraries also support
[GObject Introspection](https://gi.readthedocs.io/) to provide metadata of public API for
language bindings such as [PyGObject Python module](pygobject.readthedocs.io/).

In detail, see [Libraries](libraries.md).

## Rust crates

The team maintains crates automatically generated by [gir tool](https://gtk-rs.org/gir/book/) provided
by [gtk-rs project](https://gtk-rs.org/), which parses the library metadata for crate generation.

In detail, see [Rust crates](crates.md).

## Applications

At present the team maintains some service programs to operate audio and music units
in IEEE 1394 bus supported by ALSA firewire stack for their model specific functionalities.

In detail, see [Applications](applications.md).

## Support

* Please file your issues into each github repository if finding it.
* Post messages to [alsa-devel mailing list](https://mailman.alsa-project.org/mailman/listinfo/alsa-devel)
* The other users will probably have interests in your issue, thus let us to share the issue
  instead of direct contact to indivisual developer.

## Documentation repository

This documentation is hosted in <https://github.com/alsa-project/gobject-introspection-docs/>.
