## WTPM - Software TPM Emulator
------------

The `swTPM` package provides TPM emulators with different front-end interfaces
to `libtpms`. TPM emulators provide socket interfaces (TCP/IP and Unix) and
the Linux CUSE interface for the creation of multiple native `/dev/vtpm*` devices.

The `swTPM` package also provides several tools for using the TPM emulator,
creating certificates for a TPM, and simulating the manufacturing of
a TPM by creating a TPM's EK and platform certificates etc. Please read 
the `README`'s in the individual tool's directory under `src/`

#### Please consult the Wiki for information about swTPM:

   <https://github.com/stefanberger/swtpm/wiki>
