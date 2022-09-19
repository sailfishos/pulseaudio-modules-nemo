check_mainvolume = executable('check_mainvolume',
  'check_mainvolume.c',
  include_directories : [configinc, meego_mainvolume_inc, srcinc],
  install_rpath : rpath_dirs,
  dependencies : [check_dep, meego_common_dep, meego_mainvolume_dep],
  name_prefix : ''
)

test('check_mainvolume', check_mainvolume)
