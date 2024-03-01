# short-term-store
Very basic storage, with timeout.
Intended to allow an application that requires external data to restart after a panic or similar outage.

# Import
import "github.com/paul-at-nangalan/short-term-store/store"

# Usage
Objects that want to be stored must implement the Encoder and Decoder interface.

To provide storage a type needs to implement the Store interface, see FileStore implementation.

# FileStore

FileStore is designed to create the storage in memory and then write it to disk in a seperate thread,
so as to minimilse the impact on the main thread.