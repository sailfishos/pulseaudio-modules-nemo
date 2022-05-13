meego_sidetone_sources = [
  'alsa-utils.c',
  'alsa-util-old.c',
  'ctrl-element.c',
  'module-meego-sidetone.c',
  'sidetone.c',
  'sidetone-args.c',
]

meego_sidetone = library('module-meego-sidetone',
  meego_sidetone_sources,
  c_args : [pa_c_args, '-DPA_MODULE_NAME=module_meego_sidetone'],
  install : true,
  install_dir : modlibexecdir,
  install_rpath : rpath_dirs,
  dependencies : [meego_common_dep],
  name_prefix : ''
)

meego_sidetone_inc = include_directories('.')

meego_sidetone_dep = declare_dependency(
  link_with : meego_sidetone,
  compile_args : pa_c_args,
  dependencies : libmeego_common_deps,
  include_directories : [configinc, libmeego_common_inc],
)

subdir('tests')
