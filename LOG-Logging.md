Logging
=======

Opening Log Files
-----------------

```
# log.open_file = "log name", "file path"
log.open_file = "rtorrent.log", (cat,/tmp/rtorrent.log.,(system.pid))  
```

A newly opened log file is not connected to any logging events.

Some control over formatting will be provided at a later date.

Adding outputs to events
------------------------

```
    # log.add_output = "logging event", "log name"

    log.add_output = "info", "rtorrent.log"

    log.add_output = "dht_debug", "tracker.log"
    log.add_output = "tracker_debug", "tracker.log"
```

Each log handle can be added to multiple different logging events.

Logging events
--------------

```
    "critical"
    "error"
    "warn"
    "notice"
    "info"
    "debug"
```

The above events receive logging events from all the sub-groups
displayed below, and each event also receives events from the event
above in importance.

Thus some high-volume sub-group events such as “tracker\_debug” are not
part of “debug” and every “warn” event will receive events from “error”,
“critical”.

    critical
    error
    warn
    notice
    info
    debug
    dht_critical
    dht_error
    dht_warn
    dht_notice
    dht_info
    dht_debug
    peer_critical
    peer_error
    peer_warn
    peer_notice
    peer_info
    peer_debug
    socket_critical
    socket_error
    socket_warn
    socket_notice
    socket_info
    socket_debug
    storage_critical
    storage_error
    storage_warn
    storage_notice
    storage_info
    storage_debug
    thread_critical
    thread_error
    thread_warn
    thread_notice
    thread_info
    thread_debug
    tracker_critical
    tracker_error
    tracker_warn
    tracker_notice
    tracker_info
    tracker_debug
    torrent_critical
    torrent_error
    torrent_warn
    torrent_notice
    torrent_info
    torrent_debug
    
    connection
    connection_bind
    connection_fd
    connection_filter
    connection_hanshake
    connection_listen
    dht_all
    dht_manager
    dht_node
    dht_router
    dht_server
    instrumentation_memory
    instrumentation_mincore
    instrumentation_choke
    instrumentation_polling
    instrumentation_transfers
    peer_list_events
    protocol_piece_events
    protocol_metadata_events
    protocol_network_errors
    protocol_storage_errors
    resume_data
    rpc_events
    rpc_dump
    ui_events
