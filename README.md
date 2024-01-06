# raft-ebpf-veilid
A group of linux ebpf *and* userland programs, to sync writes to files, while using veilid for messaging to negotiate raft elections and log replication.

## TODO
* [ ] RAFT: election over veilid
* [ ] RAFT: heart beats
* [ ] RAFT: log replication
* [ ] eBPF: communicate events and allow certain system calls between userland veilid server and eBPF program.
* [ ] Initially, apply to unmodified journalled (e.g. WAL etc) sqlite, and intercept system calls, eBPF sends events to veilid server via mmap, veilid server and allows / aborts each system call, based on follower consensus.
* [ ] Bonus: pass messages via io uring, I have no frikking clue how to do this on veilid.

## Main goals
* [ ] Learn raft, veilid, eBPF
* [ ] Ideally, apply replication to any database, or any file, anywhere, become storage medium agnostic.

## Languages
The proof of concept for raft will be mainly written in rust and C. Who knows, maybe zig.
