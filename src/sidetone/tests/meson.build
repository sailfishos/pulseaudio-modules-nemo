check_sidetone = executable('check_sidetone',
  'check_sidetone.c',
  include_directories : [configinc, meego_sidetone_inc, srcinc],
  install_rpath : rpath_dirs,
  dependencies : [check_dep, meego_common_dep, meego_sidetone_dep],
  name_prefix : ''
)

test('check_sidetone', check_sidetone)
