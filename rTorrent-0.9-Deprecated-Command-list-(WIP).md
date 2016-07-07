# The commands in the list below are deprecated.
#### Their use is highly discouraged, as they will become obsolete and are subject to removal at any time after that.


### Misc
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| encoding_list | encoding.add |
| key_layout | keys.layout.set |

### Execution
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| execute | execute2 |
| execute_nothrow | execute.nothrow |
| execute_throw | execute.throw |
| execute_raw | execute.raw |
| execute_raw_nothrow | execute.raw_nothrow |
| execute_capture | execute.capture |
| execute_capture_nothrow | execute.capture_nothrow |

### Scheduling
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| schedule | schedule2 |
| schedule_remove | schedule_remove2 |

### Directory Settings
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| get_directory | directory.default |
| directory | directory.default.set |
| set_directory | directory.default.set |

### Ratio Settings
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| ratio.disable | group.seeding.ratio.disable |
| ratio.enable | group.seeding.ratio.enable |
| ratio.max | group2.seeding.ratio.max |
| ratio.max.set | group2.seeding.ratio.max.set |
| ratio.min | group2.seeding.ratio.min |
| ratio.min.set | group2.seeding.ratio.min.set |
| ratio.upload | group2.seeding.ratio.upload |
| ratio.upload.set | group2.seeding.ratio.upload.set |

### Conversion commands
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| to_gm_date | convert.gm_date |
| to_gm_time | convert.gm_time |
| to_date | convert.date |
| to_elapsed_time | convert.elapsed_time |
| to_time | convert.time |
| to_throttle | convert.throttle |
| to_kb | convert.kb |
| to_mb | convert.mb |
| to_xb | convert.xb |

### Protocol Settings
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| get_connection_leech | protocol.connection.leech |
| connection_leech | protocol.connection.leech.set |
| set_connection_leech | protocol.connection.leech.set |
| get_connection_seed | protocol.connection.seed |
| connection_seed | protocol.connection.seed.set |
| set_connection_seed | protocol.connection.seed.set |
| encryption | protocol.encryption.set |
| get_peer_exchange | protocol.pex |
| peer_exchange | protocol.pex.set |
| set_peer_exchange | protocol.pex.set |

### Memory/Pieces Settings
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| get_memory_usage | pieces.memory.current |
| get_max_memory_usage | pieces.memory.max |
| max_memory_usage | pieces.memory.max.set |
| set_max_memory_usage | pieces.memory.max.set |
| get_check_hash | pieces.hash.on_completion |
| check_hash | pieces.hash.on_completion.set |
| set_check_hash | pieces.hash.on_completion.set |
| get_preload_type | pieces.preload.type |
| get_preload_min_size | pieces.preload.min_size |
| set_preload_min_size | pieces.preload.min_size.set |
| get_preload_required_rate | pieces.preload.min_rate |
| set_preload_required_rate | pieces.preload.min_rate.set |
| set_preload_type | pieces.preload.type.set |
| get_stats_preloaded | pieces.stats_preloaded |
| get_stats_not_preloaded | pieces.stats_not_preloaded |
| get_safe_sync | pieces.sync.always_safe |
| set_safe_sync | pieces.sync.always_safe.set |
| get_timeout_sync | pieces.sync.timeout |
| set_timeout_sync | pieces.sync.timeout.set |
| get_timeout_safe_sync | pieces.sync.timeout_safe |
| set_timeout_safe_sync | pieces.sync.timeout_safe.set |

### Throttle Settings
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| throttle_down | throttle.down |
| get_throttle_down_max | throttle.down.max |
| get_throttle_down_rate | throttle.down.rate |
| get_download_rate | throttle.global_down.max_rate |
| set_download_rate | throttle.global_down.max_rate.set |
| download_rate | throttle.global_down.max_rate.set_kb |
| get_down_rate | throttle.global_down.rate |
| get_down_total | throttle.global_down.total |
| get_upload_rate | throttle.global_up.max_rate |
| set_upload_rate | throttle.global_up.max_rate.set |
| upload_rate | throttle.global_up.max_rate.set_kb |
| get_up_rate | throttle.global_up.rate |
| get_up_total | throttle.global_up.total |
| throttle_ip | throttle.ip |
| max_downloads | throttle.max_downloads.set |
| get_max_downloads_div | throttle.max_downloads.div |
| max_downloads_div | throttle.max_downloads.div.set |
| set_max_downloads_div | throttle.max_downloads.div.set |
| get_max_downloads_global | throttle.max_downloads.global |
| max_downloads_global | throttle.max_downloads.global.set |
| set_max_downloads_global | throttle.max_downloads.global.set |
| get_max_peers | throttle.max_peers.normal |
| max_peers | throttle.max_peers.normal.set |
| set_max_peers | throttle.max_peers.normal.set |
| get_max_peers_seed | throttle.max_peers.seed |
| max_peers_seed | throttle.max_peers.seed.set |
| set_max_peers_seed | throttle.max_peers.seed.set |
| get_max_uploads | throttle.max_uploads |
| max_uploads | throttle.max_uploads.set |
| set_max_uploads | throttle.max_uploads.set |
| get_max_uploads_div | throttle.max_uploads.div |
| max_uploads_div | throttle.max_uploads.div.set |
| set_max_uploads_div | throttle.max_uploads.div.set |
| get_max_uploads_global | throttle.max_uploads.global |
| max_uploads_global | throttle.max_uploads.global.set |
| set_max_uploads_global | throttle.max_uploads.global.set |
| min_downloads | throttle.min_downloads.set |
| get_min_peers | throttle.min_peers.normal |
| min_peers | throttle.min_peers.normal.set |
| set_min_peers | throttle.min_peers.normal.set |
| get_min_peers_seed | throttle.min_peers.seed |
| min_peers_seed | throttle.min_peers.seed.set |
| set_min_peers_seed | throttle.min_peers.seed.set |
| min_uploads | throttle.min_uploads.set |
| throttle_up | throttle.up |
| get_throttle_up_max | throttle.up.max |
| get_throttle_up_rate | throttle.up.rate |

### DHT Settings
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| dht_add_node | dht.add_node |
| dht | dht.mode.set |
| get_dht_port | dht.port |
| dht_port | dht.port.set |
| set_dht_port | dht.port.set |
| get_dht_throttle | dht.throttle.name |
| set_dht_throttle | dht.throttle.name.set |
| dht_statistics | dht.statistics |

### Network Settings
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| bind | network.bind_address.set |
| ip | network.local_address.set |
| port_random | network.port_random.set |
| port_range | network.port_range.set |
| proxy_address | network.proxy_address.set |
| scgi_port | network.scgi.open_port |
| scgi_local | network.scgi.open_local |
| set_bind | network.bind_address.set |
| get_bind | network.bind_address |
| get_http_capath | network.http.capath |
| http_capath | network.http.capath.set |
| set_http_capath | network.http.capath.set |
| get_http_cacert | network.http.cacert |
| http_cacert | network.http.cacert.set |
| set_http_cacert | network.http.cacert.set |
| get_max_open_http | network.http.max_open |
| set_max_open_http | network.http.max_open.set |
| get_http_proxy | network.http.proxy_address |
| http_proxy | network.http.proxy_address.set |
| set_http_proxy | network.http.proxy_address.set |
| set_ip | network.local_address.set |
| get_ip | network.local_address |
| get_max_open_files | network.max_open_files |
| set_max_open_files | network.max_open_files.set |
| get_max_open_sockets | network.max_open_sockets |
| port_open | network.port_open.set |
| get_port_open | network.port_open |
| set_port_open | network.port_open.set |
| get_port_random | network.port_random |
| set_port_random | network.port_random.set |
| get_port_range | network.port_range |
| set_port_range | network.port_range.set |
| set_proxy_address | network.proxy_address.set |
| get_proxy_address | network.proxy_address |
| get_receive_buffer_size | network.receive_buffer.size |
| set_receive_buffer_size | network.receive_buffer.size.set |
| set_scgi_dont_route | network.scgi.dont_route.set |
| get_scgi_dont_route | network.scgi.dont_route |
| get_send_buffer_size | network.send_buffer.size |
| set_send_buffer_size | network.send_buffer.size.set |
| set_xmlrpc_dialect | network.xmlrpc.dialect.set |
| xmlrpc_dialect | network.xmlrpc.dialect.set |
| get_xmlrpc_size_limit | network.xmlrpc.size_limit |
| set_xmlrpc_size_limit | network.xmlrpc.size_limit.set |
| xmlrpc_size_limit | network.xmlrpc.size_limit.set |

### Session Settings
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| get_session | session.path |
| set_session | session.path.set |
| session | session.path.set |
| session_save | session.save |
| get_name | session.name |
| set_name | session.name.set |
| get_session_on_completion | session.on_completion |
| set_session_on_completion | session.on_completion.set |
| get_session_lock | session.use_lock |
| set_session_lock | session.use_lock.set |

### Method Commands
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| system.method.insert | method.insert |
| system.method.erase | method.erase |
| system.method.get | method.get |
| system.method.set | method.set |
| system.method.list_keys | method.list_keys |
| system.method.has_key | method.has_key |
| system.method.set_key | method.set_key |

### System Settings
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| system.file_allocate | system.file.allocate |
| system.file_allocate.set | system.file.allocate.set |
| get_max_file_size | system.file.max_size |
| set_max_file_size | system.file.max_size.set |
| get_split_file_size | system.file.split_size |
| set_split_file_size | system.file.split_size.set |
| get_split_suffix | system.file.split_suffix |
| set_split_suffix | system.file.split_suffix.set |

### Load Commands
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| load | load.normal |
| load_start | load.start |
| load_start_verbose | load.start_verbose |
| load_raw | load.raw |
| load_raw_start | load.raw_start |
| load_raw_verbose | load.raw_verbose |
| load_verbose | load.verbose |

### Tracker Settings
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| get_tracker_numwant | trackers.numwant |
| set_tracker_numwant | trackers.numwant.set |
| tracker_numwant | trackers.numwant.set |
| get_use_udp_trackers | trackers.use_udp |
| set_use_udp_trackers | trackers.use_udp.set |
| use_udp_trackers | trackers.use_udp.set |

### Download Commands/Variables
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| d.get_hash | d.hash |
| d.get_local_id | d.local_id |
| d.get_local_id_html | d.local_id_html |
| d.get_bitfield | d.bitfield |
| d.get_base_path | d.base_path |
| d.get_base_filename | d.base_filename |
| d.get_name | d.name |
| d.get_creation_date | d.creation_date |
| d.get_peer_exchange | d.peer_exchange |
| d.get_up_rate | d.up.rate |
| d.get_up_total | d.up.total |
| d.get_down_rate | d.down.rate |
| d.get_down_total | d.down.total |
| d.get_skip_rate | d.skip.rate |
| d.get_skip_total | d.skip.total |
| d.get_bytes_done | d.bytes_done |
| d.get_chunk_size | d.chunk_size |
| d.get_chunks_hashed | d.chunks_hashed |
| d.get_complete | d.complete |
| d.get_completed_bytes | d.completed_bytes |
| d.get_completed_chunks | d.completed_chunks |
| d.get_connection_current | d.connection_current |
| d.get_connection_leech | d.connection_leech |
| d.get_connection_seed | d.connection_seed |
| d.get_custom | d.custom |
| d.get_custom1 | d.custom1 |
| d.get_custom2 | d.custom2 |
| d.get_custom3 | d.custom3 |
| d.get_custom4 | d.custom4 |
| d.get_custom5 | d.custom5 |
| d.get_custom_throw | d.custom_throw |
| d.get_directory | d.directory |
| d.get_directory_base | d.directory_base |
| d.get_free_diskspace | d.free_diskspace |
| d.get_hashing | d.hashing |
| d.get_hashing_failed | d.hashing_failed |
| d.get_ignore_commands | d.ignore_commands |
| d.get_left_bytes | d.left_bytes |
| d.get_loaded_file | d.loaded_file |
| d.get_max_file_size | d.max_file_size |
| d.get_max_size_pex | d.max_size_pex |
| d.get_message | d.message |
| d.get_mode | d.mode |
| d.get_peers_accounted | d.peers_accounted |
| d.get_peers_complete | d.peers_complete |
| d.get_peers_connected | d.peers_connected |
| d.get_peers_max | d.peers_max |
| d.get_peers_min | d.peers_min |
| d.get_peers_not_connected | d.peers_not_connected |
| d.get_priority | d.priority |
| d.get_priority_str | d.priority_str |
| d.get_ratio | d.ratio |
| d.get_size_bytes | d.size_bytes |
| d.get_size_chunks | d.size_chunks |
| d.get_size_files | d.size_files |
| d.get_size_pex | d.size_pex |
| d.get_state | d.state |
| d.get_state_changed | d.state_changed |
| d.get_state_counter | d.state_counter |
| d.get_throttle_name | d.throttle_name |
| d.get_tied_to_file | d.tied_to_file |
| d.get_tracker_focus | d.tracker_focus |
| d.get_tracker_numwant | d.tracker_numwant |
| d.get_tracker_size | d.tracker_size |
| d.get_uploads_max | d.uploads_max |
| d.set_connection_current | d.connection_current.set |
| d.set_custom | d.custom.set |
| d.set_custom1 | d.custom1.set |
| d.set_custom2 | d.custom2.set |
| d.set_custom3 | d.custom3.set |
| d.set_custom4 | d.custom4.set |
| d.set_custom5 | d.custom5.set |
| d.set_directory | d.directory.set |
| d.set_directory_base | d.directory_base.set |
| d.set_hashing_failed | d.hashing_failed.set |
| d.set_ignore_commands | d.ignore_commands.set |
| d.set_max_file_size | d.max_file_size.set |
| d.set_message | d.message.set |
| d.set_peers_max | d.peers_max.set |
| d.set_peers_min | d.peers_min.set |
| d.set_priority | d.priority.set |
| d.set_throttle_name | d.throttle_name.set |
| d.set_tied_to_file | d.tied_to_file.set |
| d.set_tracker_numwant | d.tracker_numwant.set |
| d.set_uploads_max | d.uploads_max.set |
| create_link | d.create_link |
| delete_link | d.delete_link |
| delete_tied | d.delete_tied |
| d.multicall | d.multicall2 |

### Torrent Commands/Variables
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| t.get_group | t.group |
| t.get_id | t.id |
| t.get_min_interval | t.min_interval |
| t.get_normal_interval | t.normal_interval |
| t.get_scrape_complete | t.scrape_complete |
| t.get_scrape_downloaded | t.scrape_downloaded |
| t.get_scrape_incomplete | t.scrape_incomplete |
| t.get_scrape_time_last | t.scrape_time_last |
| t.get_type | t.type |
| t.get_url | t.url |
| t.set_enabled | t.is_enabled.set |

### File Commands/Variables
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| f.get_completed_chunks | f.completed_chunks |
| f.get_frozen_path | f.frozen_path |
| f.get_last_touched | f.last_touched |
| f.get_match_depth_next | f.match_depth_next |
| f.get_match_depth_prev | f.match_depth_prev |
| f.get_offset | f.offset |
| f.get_path | f.path |
| f.get_path_components | f.path_components |
| f.get_path_depth | f.path_depth |
| f.get_priority | f.priority |
| f.get_range_first | f.range_first |
| f.get_range_second | f.range_second |
| f.get_size_bytes | f.size_bytes |
| f.get_size_chunks | f.size_chunks |
| f.set_priority | f.priority.set |
| fi.get_filename_last | fi.filename_last |

### Peer Commands/Variables
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| p.get_address | p.address |
| p.get_client_version | p.client_version |
| p.get_completed_percent | p.completed_percent |
| p.get_down_rate | p.down_rate |
| p.get_down_total | p.down_total |
| p.get_id | p.id |
| p.get_id_html | p.id_html |
| p.get_options_str | p.options_str |
| p.get_peer_rate | p.peer_rate |
| p.get_peer_total | p.peer_total |
| p.get_port | p.port |
| p.get_up_rate | p.up_rate |
| p.get_up_total | p.up_total |

### View Commands/Variables
| Deprecated Command | Replacement |
| ------------------ | ----------- |
| view_add | view.add |
| view_filter | view.filter |
| view_filter_on | view.filter_on |
| view_list | view.list |
| view_set | view.set |
| view_sort | view.sort |
| view_sort_current | view.sort_current |
| view_sort_new | view.sort_new |

