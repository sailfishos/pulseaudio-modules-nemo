module_stream_restore_nemo = library('module-stream-restore-nemo',
  'module-stream-restore-nemo.c',
  c_args : [pa_c_args, '-DPA_MODULE_NAME=module_stream_restore_nemo'],
  link_args : ['-L'+libdir+'/pulse-'+pa_version_major_minor+'/modules', '-lprotocol-native'],
  install : true,
  install_dir : modlibexecdir,
  install_rpath : rpath_dirs,
  dependencies : [meego_common_dep],
  name_prefix : ''
)
