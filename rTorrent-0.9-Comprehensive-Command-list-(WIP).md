# Comprehensive list of rTorrent 0.9 commands
#### Use of the deprecated commands is highly discouraged as those commands are subject to removal at any time.

### Operators
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `if` | - | Evaluates a condition to be either true or false and takes action based on that |
| `not` | - | Inversion of `if` Evaluates a condition to be either NOT true or NOT false and takes action based on that |
| `false` | - | Always returns false - used when you want to take action on something being false |
| `and` | - | Evaluates 2 or more conditions and takes action based on whether both are true or if one is false |
| `or` | - | Evaluates 2 or more conditions and takes action based on whether one is true, or both are false |

### Misc
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `encoding.add` | `encoding_list` | Configure filename encodings |
| `keys.layout.set` | `key_layout` | Define keyboard layout for key bindings `<qwerty|azerty|qwertz|dvorak>` |

### Execution
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `execute2` | `execute` | See [COMMAND Execute](https://github.com/rakshasa/rtorrent/wiki/COMMAND-Execute) -- Tilde gets special treatment |
| `execute.throw` | `execute_throw` | Same as above |
| `execute.throw.bg` |  | Same as above but run the command in the background |
| `execute.nothrow` | `execute_nothrow` | See [COMMAND Execute](https://github.com/rakshasa/rtorrent/wiki/COMMAND-Execute) |
| `execute.nothrow.bg` |  | Same as above but run the command in the background |
| `execute.capture` | `execute_capture` | See [COMMAND Execute](https://github.com/rakshasa/rtorrent/wiki/COMMAND-Execute) |
| `execute.capture_nothrow` | `execute_capture_nothrow` | Same as above |
| `execute.raw` | `execute_raw` | See [COMMAND Execute](https://github.com/rakshasa/rtorrent/wiki/COMMAND-Execute) -- Tilde does not get special treatment |
| `execute.raw.bg` |  | Same as above but run the command in the background |
| `execute.raw_nothrow` | `execute_raw_nothrow` | [COMMAND Execute](https://github.com/rakshasa/rtorrent/wiki/COMMAND-Execute) |
| `execute.raw_nothrow.bg` |  | Same as above but run the command in the background |

### Scheduling
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `schedule2` | `schedule` | See [COMMAND Scheduling](https://github.com/rakshasa/rtorrent/wiki/COMMAND-Scheduling) |
| `schedule_remove2` | `schedule_remove` | See [COMMAND Scheduling](https://github.com/rakshasa/rtorrent/wiki/COMMAND-Scheduling) |

### Directory
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `directory.default` | `get_directory` | Prints the default directory for downloaded torrent data |
| `directory.default.set` | `directory` | Sets the default directory for downloaded torrent data |
| `directory.default.set` | `set_directory` | Same as above |

### Ratio
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `group.seeding.ratio.disable` | `ratio.disable` | |
| `group.seeding.ratio.enable` | `ratio.enable` | |
| `group2.seeding.ratio.max` | `ratio.max` | |
| `group2.seeding.ratio.max.set` | `ratio.max.set` | |
| `group2.seeding.ratio.min` | `ratio.min` | |
| `group2.seeding.ratio.min.set` | `ratio.min.set` | |
| `group2.seeding.ratio.upload`	| `ratio.upload` | |
| `group2.seeding.ratio.upload.set` | `ratio.upload.set` | |

### Conversion
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `convert.date` | `to_date` | |
| `convert.elapsed_time` | `to_elapsed_time` | |
| `convert.gm_date` | `to_gm_date` | |
| `convert.gm_time` | `to_gm_time` | |
| `convert.kb` | `to_kb` | |
| `convert.mb` | `to_mb` | |
| `convert.time` | `to_time` | |
| `convert.throttle` | `to_throttle` | |
| `convert.xb` | `to_xb` | |

### Protocol
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `protocol.connection.leech` | `get_connection_leech` | |
| `protocol.connection.leech.set` | `connection_leech` | |
| `protocol.connection.leech.set` | `set_connection_leech` | |
| `protocol.connection.seed` | `get_connection_seed` | |
| `protocol.connection.seed.set` | `connection_seed` | |
| `protocol.connection.seed.set` | `set_connection_seed` | |
| `protocol.encryption.set` | `encryption` | |
| `protocol.pex` | `get_peer_exchange` | |
| `protocol.pex.set` | `peer_exchange` | |
| `protocol.pex.set` | `set_peer_exchange` | |

### Memory/Pieces
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `pieces.memory.current` | `get_memory_usage` | |
| `pieces.memory.max` | `get_max_memory_usage` | |
| `pieces.memory.max.set` | `max_memory_usage` | |
| `pieces.memory.max.set` | `set_max_memory_usage` | |
| `pieces.hash.on_completion` | `get_check_hash` | |
| `pieces.hash.on_completion.set` | `check_hash` | |
| `pieces.hash.on_completion.set` | `set_check_hash` | |
| `pieces.preload.type` | `get_preload_type` | |
| `pieces.preload.min_size` | `get_preload_min_size` | |
| `pieces.preload.min_size.set` | `set_preload_min_size` | |
| `pieces.preload.min_rate` | `get_preload_required_rate` | |
| `pieces.preload.min_rate.set` | `set_preload_required_rate` | |
| `pieces.preload.type.set` | `set_preload_type` | |
| `pieces.stats_preloaded` | `get_stats_preloaded` | |
| `pieces.stats_not_preloaded` | `get_stats_not_preloaded` | |
| `pieces.sync.always_safe` | `get_safe_sync` | |
| `pieces.sync.always_safe.set` | `set_safe_sync` | |
| `pieces.sync.timeout` | `get_timeout_sync` | |
| `pieces.sync.timeout.set` | `set_timeout_sync` | |
| `pieces.sync.timeout_safe` | `get_timeout_safe_sync` | |
| `pieces.sync.timeout_safe.set` | `set_timeout_safe_sync` | |

### Throttle
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `throttle.down` | `throttle_down` | |
| `throttle.down.max` | `get_throttle_down_max` | |
| `throttle.down.rate` | `get_throttle_down_rate` | |
| `throttle.global_down.max_rate` | `get_download_rate` | |
| `throttle.global_down.max_rate.set` | `set_download_rate` | |
| `throttle.global_down.max_rate.set_kb` | `download_rate` | |
| `throttle.global_down.rate` | `get_down_rate` | |
| `throttle.global_down.total` | `get_down_total` | |
| `throttle.global_up.max_rate` | `get_upload_rate` | |
| `throttle.global_up.max_rate.set` | `set_upload_rate` | |
| `throttle.global_up.max_rate.set_kb` | `upload_rate` | |
| `throttle.global_up.rate` | `get_up_rate` | |
| `throttle.global_up.total` | `get_up_total` | |
| `throttle.ip` | `throttle_ip` | |
| `throttle.max_downloads.set` | `max_downloads` | |
| `throttle.max_downloads.div` | `get_max_downloads_div` | |
| `throttle.max_downloads.div.set` | `max_downloads_div` | |
| `throttle.max_downloads.div.set` | `set_max_downloads_div` | |
| `throttle.max_downloads.global` | `get_max_downloads_global` | |
| `throttle.max_downloads.global.set` | `max_downloads_global` | |
| `throttle.max_downloads.global.set` | `set_max_downloads_global` | |
| `throttle.max_peers.normal` | `get_max_peers` | |
| `throttle.max_peers.normal.set` | `max_peers` | |
| `throttle.max_peers.normal.set` | `set_max_peers` | |
| `throttle.max_peers.seed` | `get_max_peers_seed` | |
| `throttle.max_peers.seed.set` | `max_peers_seed` | |
| `throttle.max_peers.seed.set` | `set_max_peers_seed` | |
| `throttle.max_uploads` | `get_max_uploads` | |
| `throttle.max_uploads.set` | `max_uploads` | |
| `throttle.max_uploads.set` | `set_max_uploads` | |
| `throttle.max_uploads.div` | `get_max_uploads_div` | |
| `throttle.max_uploads.div.set` | `max_uploads_div` | |
| `throttle.max_uploads.div.set` | `set_max_uploads_div` | |
| `throttle.max_uploads.global` | `get_max_uploads_global` | |
| `throttle.max_uploads.global.set` | `max_uploads_global` | |
| `throttle.max_uploads.global.set` | `set_max_uploads_global` | |
| `throttle.min_downloads.set` | `min_downloads` | |
| `throttle.min_peers.normal` | `get_min_peers` | |
| `throttle.min_peers.normal.set` | `min_peers` | |
| `throttle.min_peers.normal.set` | `set_min_peers` | |
| `throttle.min_peers.seed` | `get_min_peers_seed` | |
| `throttle.min_peers.seed.set` | `min_peers_seed` | |
| `throttle.min_peers.seed.set` | `set_min_peers_seed` | |
| `throttle.min_uploads.set` | `min_uploads` | |
| `throttle.up` | `throttle_up` | |
| `throttle.up.max` | `get_throttle_up_max` | |
| `throttle.up.rate` | `get_throttle_up_rate` | |

### DHT
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `dht.add_node` | `dht_add_node` | |
| `dht.mode.set` | `dht` | |
| `dht.port` | `get_dht_port` | |
| `dht.port.set` | `dht_port` | |
| `dht.port.set` | `set_dht_port` | |
| `dht.throttle.name` | `get_dht_throttle` | |
| `dht.throttle.name.set` | `set_dht_throttle` | |
| `dht.statistics` | `dht_statistics` | |

### Network
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `network.bind_address` | `get_bind` | |
| `network.bind_address.set` | `bind` | |
| `network.bind_address.set` | `set_bind` | |
| `network.local_address` | `get_ip` | |
| `network.local_address.set` | `ip` | |
| `network.local_address.set` | `set_ip` | |
| `network.http.capath` | `get_http_capath` | |
| `network.http.capath.set` | `http_capath` | |
| `network.http.capath.set` | `set_http_capath` | |
| `network.http.cacert` | `get_http_cacert` | |
| `network.http.cacert.set` | `http_cacert` | |
| `network.http.cacert.set` | `set_http_cacert` | |
| `network.http.max_open` | `get_max_open_http` | |
| `network.http.max_open.set` | `set_max_open_http` | |
| `network.http.proxy_address` | `get_http_proxy` | |
| `network.http.proxy_address.set` | `http_proxy` | |
| `network.http.proxy_address.set` | `set_http_proxy` | |
| `network.max_open_files` | `get_max_open_files` | |
| `network.max_open_files.set` | `set_max_open_files` | |
| `network.max_open_sockets` | `get_max_open_sockets` | |
| `network.port_open` | `get_port_open` | |
| `network.port_open.set` | `port_open` | |
| `network.port_open.set` | `set_port_open` | |
| `network.port_random` | `get_port_random` | |
| `network.port_random.set` | `port_random` | |
| `network.port_random.set` | `set_port_random` | |
| `network.port_range` | `get_port_range` | |
| `network.port_range.set` | `port_range` | |
| `network.port_range.set` | `set_port_range` | |
| `network.proxy_address` | `get_proxy_address` | |
| `network.proxy_address.set` | `proxy_address` | |
| `network.proxy_address.set` | `set_proxy_address` | |
| `network.receive_buffer.size` | `get_receive_buffer_size` | |
| `network.receive_buffer.size.set` | `set_receive_buffer_size` | |
| `network.scgi.dont_route.set` | `set_scgi_dont_route` | |
| `network.scgi.dont_route` | `get_scgi_dont_route` | |
| `network.scgi.open_local` | `scgi_local` | |
| `network.scgi.open_port` | `scgi_port` | |
| `network.send_buffer.size` | `get_send_buffer_size` | |
| `network.send_buffer.size.set` | `set_send_buffer_size` | |
| `network.xmlrpc.dialect.set` | `set_xmlrpc_dialect` | |
| `network.xmlrpc.dialect.set` | `xmlrpc_dialect` | |
| `network.xmlrpc.size_limit` | `get_xmlrpc_size_limit` | |
| `network.xmlrpc.size_limit.set` | `set_xmlrpc_size_limit` | |
| `network.xmlrpc.size_limit.set` | `xmlrpc_size_limit` | |

### Session
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `session.path` | `get_session` | |
| `session.path.set` | `set_session` | |
| `session.path.set` | `session` | |
| `session.name` | `get_name` | |
| `session.name.set` | `set_name` | |
| `session.on_completion` | `get_session_on_completion` | |
| `session.on_completion.set` | `set_session_on_completion` | |
| `session.save` | `session_save` | |
| `session.use_lock` | `get_session_lock` | |
| `session.use_lock.set` | `set_session_lock` | |

### Method
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `method.insert` | `system.method.insert` | |
| `method.erase` | `system.method.erase` | |
| `method.get` | `system.method.get` | |
| `method.set` | `system.method.set` | |
| `method.list_keys` | `system.method.list_keys` | |
| `method.has_key` | `system.method.has_key` | |
| `method.set_key` | `system.method.set_key` | |

### System
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `system.file.allocate` | `system.file_allocate` | |
| `system.file.allocate.set` | `system.file_allocate.set` | |
| `system.file.max_size` | `get_max_file_size` | |
| `system.file.max_size.set` | `set_max_file_size` | |
| `system.file.split_size` | `get_split_file_size` | |
| `system.file.split_size.set` | `set_split_file_size` | |
| `system.file.split_suffix` | `get_split_suffix` | |
| `system.file.split_suffix.set` | `set_split_suffix` | |

### Load
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `load.normal` | `load` | |
| `load.start` | `load_start` | |
| `load.start_verbose` | `load_start_verbose` | |
| `load.raw` | `load_raw` | |
| `load.raw_start` | `load_raw_start` | |
| `load.raw_verbose` | `load_raw_verbose` | |
| `load.verbose` | `load_verbose` | |

### Tracker
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `trackers.numwant` | `get_tracker_numwant` | |
| `trackers.numwant.set` | `set_tracker_numwant` | |
| `trackers.numwant.set` | `tracker_numwant` | |
| `trackers.use_udp` | `get_use_udp_trackers` | |
| `trackers.use_udp.set` | `set_use_udp_trackers` | |
| `trackers.use_udp.set` | `use_udp_trackers` | |

### Downloads
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `d.base_filename` | `d.get_base_filename` | |
| `d.base_path` | `d.get_base_path` | |
| `d.bitfield` | `d.get_bitfield` | |
| `d.bytes_done` | `d.get_bytes_done` | |
| `d.chunk_size` | `d.get_chunk_size` | |
| `d.chunks_hashed` | `d.get_chunks_hashed` | |
| `d.complete` | `d.get_complete` | |
| `d.completed_bytes` | `d.get_completed_bytes` | |
| `d.completed_chunks` | `d.get_completed_chunks` | |
| `d.connection_current` | `d.get_connection_current` | |
| `d.connection_current.set` | `d.set_connection_current` | |
| `d.connection_leech` | `d.get_connection_leech` | |
| `d.connection_seed` | `d.get_connection_seed` | |
| `d.custom` | `d.get_custom` | |
| `d.custom.set` | `d.set_custom` | |
| `d.custom1` | `d.get_custom1` | |
| `d.custom1.set` | `d.set_custom1` | |
| `d.custom2` | `d.get_custom2` | |
| `d.custom2.set` | `d.set_custom2` | |
| `d.custom3` | `d.get_custom3` | |
| `d.custom3.set` | `d.set_custom3` | |
| `d.custom4` | `d.get_custom4` | |
| `d.custom4.set` | `d.set_custom4` | |
| `d.custom5` | `d.get_custom5` | |
| `d.custom5.set` | `d.set_custom5` | |
| `d.custom_throw` | `d.get_custom_throw` | |
| `d.create_link` | `create_link` | |
| `d.creation_date` | `d.get_creation_date` | |
| `d.delete_link` | `delete_link` | |
| `d.delete_tied` | `delete_tied` | |
| `d.directory` | `d.get_directory` | |
| `d.directory.set` | `d.set_directory` | |
| `d.directory_base` | `d.get_directory_base` | |
| `d.directory_base.set` | `d.set_directory_base` |
| `d.down.rate` | `d.get_down_rate` | |
| `d.down.total` | `d.get_down_total` | |
| `d.free_diskspace` | `d.get_free_diskspace` | |
| `d.hash` | `d.get_hash` | |
| `d.hashing` | `d.get_hashing` | |
| `d.hashing_failed` | `d.get_hashing_failed` | |
| `d.hashing_failed.set` | `d.set_hashing_failed` | |
| `d.ignore_commands` | `d.get_ignore_commands` | |
| `d.ignore_commands.set` | `d.set_ignore_commands` | |
| `d.left_bytes` | `d.get_left_bytes` | |
| `d.local_id` | `d.get_local_id` | |
| `d.local_id_html` | `d.get_local_id_html` | |
| `d.loaded_file` | `d.get_loaded_file` | |
| `d.max_file_size` | `d.get_max_file_size` | |
| `d.max_file_size.set` | `d.set_max_file_size` | |
| `d.max_size_pex` | `d.get_max_size_pex` | |
| `d.message` | `d.get_message` | |
| `d.message.set` | `d.set_message` | |
| `d.mode` | `d.get_mode` | |
| `d.multicall2` | `d.multicall` | |
| `d.name` | `d.get_name` | |
| `d.peer_exchange` | `d.get_peer_exchange` | |
| `d.peers_accounted` | `d.get_peers_accounted` | |
| `d.peers_complete` | `d.get_peers_complete` | |
| `d.peers_connected` | `d.get_peers_connected` | |
| `d.peers_max` | `d.get_peers_max` | |
| `d.peers_max.set` | `d.set_peers_max` | |
| `d.peers_min` | `d.get_peers_min` | |
| `d.peers_min.set` | `d.set_peers_min` | |
| `d.peers_not_connected` | `d.get_peers_not_connected` | |
| `d.priority` | `d.get_priority` | |
| `d.priority.set` | `d.set_priority` | |
| `d.priority_str` | `d.get_priority_str` | |
| `d.ratio` | `d.get_ratio` | |
| `d.size_bytes` | `d.get_size_bytes` | |
| `d.size_chunks` | `d.get_size_chunks` | |
| `d.size_files` | `d.get_size_files` | |
| `d.size_pex` | `d.get_size_pex` | |
| `d.skip.rate` | `d.get_skip_rate` | |
| `d.skip.total` | `d.get_skip_total` | |
| `d.state` | `d.get_state` | |
| `d.state_changed` | `d.get_state_changed` | |
| `d.state_counter` | `d.get_state_counter` | |
| `d.throttle_name` | `d.get_throttle_name` | |
| `d.throttle_name.set` | `d.set_throttle_name` | |
| `d.tied_to_file` | `d.get_tied_to_file` | |
| `d.tied_to_file.set` | `d.set_tied_to_file` | |
| `d.tracker_focus` | `d.get_tracker_focus` | |
| `d.tracker_numwant` | `d.get_tracker_numwant` | |
| `d.tracker_numwant.set` | `d.set_tracker_numwant` | |
| `d.tracker_size` | `d.get_tracker_size` | |
| `d.up.rate` | `d.get_up_rate` | |
| `d.up.total` | `d.get_up_total` | |
| `d.uploads_max` | `d.get_uploads_max` | |
| `d.uploads_max.set` | `d.set_uploads_max` | |

### Torrents
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `t.group` | `t.get_group` | |
| `t.id` | `t.get_id` | |
| `t.is_enabled.set` | `t.set_enabled` | |
| `t.min_interval` | `t.get_min_interval` | |
| `t.normal_interval` | `t.get_normal_interval` | |
| `t.scrape_complete` | `t.get_scrape_complete` | |
| `t.scrape_downloaded` | `t.get_scrape_downloaded` | |
| `t.scrape_incomplete` | `t.get_scrape_incomplete` | |
| `t.scrape_time_last` | `t.get_scrape_time_last` | |
| `t.type` | `t.get_type` | |
| `t.url` | `t.get_url` | |

### Files
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `f.completed_chunks` | `f.get_completed_chunks` | |
| `f.frozen_path` | `f.get_frozen_path` | |
| `f.last_touched` | `f.get_last_touched` | |
| `f.match_depth_next` | `f.get_match_depth_next` | |
| `f.match_depth_prev` | `f.get_match_depth_prev` | |
| `f.offset` | `f.get_offset` | |
| `f.path` | `f.get_path` | |
| `f.path_components` | `f.get_path_components` | |
| `f.path_depth` | `f.get_path_depth` | |
| `f.priority` | `f.get_priority` | |
| `f.range_first` | `f.get_range_first` | |
| `f.range_second` | `f.get_range_second` | |
| `f.size_bytes` | `f.get_size_bytes` | |
| `f.size_chunks` | `f.get_size_chunks` | |
| `f.priority.set` | `f.set_priority` | |
| `fi.filename_last` | `fi.get_filename_last` | |

### Peers
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `p.address` | `p.get_address` | |
| `p.client_version` | `p.get_client_version` | |
| `p.completed_percent` | `p.get_completed_percent` | |
| `p.down_rate` | `p.get_down_rate` | |
| `p.down_total` | `p.get_down_total` | |
| `p.id` | `p.get_id` | |
| `p.id_html` | `p.get_id_html` | |
| `p.options_str` | `p.get_options_str` | |
| `p.peer_rate` | `p.get_peer_rate` | |
| `p.peer_total` | `p.get_peer_total` | |
| `p.port` | `p.get_port` | |
| `p.up_rate` | `p.get_up_rate` | |
| `p.up_total` | `p.get_up_total` | |

### Views
| Command | Deprecated Commands | Description |
| ------- | ------------------- | ----------- |
| `view.add` | `view_add` | |
| `view.filter` | `view_filter` | |
| `view.filter_on` | `view_filter_on` | |
| `view.list` | `view_list` | |
| `view.set` | `view_set` | |
| `view.sort` | `view_sort` | |
| `view.sort_current` | `view_sort_current` | |
| `view.sort_new` | `view_sort_new` | |
