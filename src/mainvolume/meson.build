meego_mainvolume_sources = [
  'mainvolume.c',
  'listening-watchdog.c',
  'module-meego-mainvolume.c',
]

meego_mainvolume = library('module-meego-mainvolume',
  meego_mainvolume_sources,
  c_args : [pa_c_args, '-DPA_MODULE_NAME=module_meego_mainvolume'],
  install : true,
  install_dir : modlibexecdir,
  install_rpath : rpath_dirs,
  dependencies : [meego_common_dep],
  name_prefix : ''
)

meego_mainvolume_dep = declare_dependency(
  link_with : meego_mainvolume,
  compile_args : pa_c_args,
  dependencies : libmeego_common_deps,
  include_directories : [configinc, libmeego_common_inc],
)
