meego_test_parameters = library('module-meego-test-parameters',
  'module-meego-test-parameters.c',
  c_args : [pa_c_args, '-DPA_MODULE_NAME=module_meego_test_parameters'],
  include_directories : [configinc, srcinc],
#  install : true,
  install_dir : modlibexecdir,
  install_rpath : rpath_dirs,
  dependencies : [meego_common_dep],
  name_prefix : ''
)
