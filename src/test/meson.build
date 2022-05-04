module_meego_test = shared_module('module-meego-test',
  'module-meego-test.c',
  c_args : [pa_c_args, '-DPA_MODULE_NAME=module_meego_test'],
  install : true,
  install_dir : modlibexecdir,
  install_rpath : rpath_dirs,
  dependencies : [meego_common_dep],
  name_prefix : ''
)
