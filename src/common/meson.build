libmeego_common_sources = [
  'algorithm-hook.c',
  'algorithm-base.c',
  'call-state-tracker.c',
  'memory.c',
  'optimized.c',
  'pa-optimized.c',
  'parameter-hook.c',
  'shared-data.c',
  'volume-proxy.c',
  'src-8-to-48.c',
  'src-48-to-8.c',
  'src-16-to-48.c',
  'src-48-to-16.c',
]

libmeego_common_meego_headers = [
  'include/meego/algorithm-base.h',
  'include/meego/algorithm-hook.h',
  'include/meego/call-state-tracker.h',
  'include/meego/memory.h',
  'include/meego/optimized.h',
  'include/meego/pa-optimized.h',
  'include/meego/parameter-hook.h',
  'include/meego/parameter-hook-implementor.h',
  'include/meego/parameter-modifier.h',
  'include/meego/proplist-meego.h',
  'include/meego/shared-data.h',
  'include/meego/volume-proxy.h',
]

install_headers(
  libmeego_common_meego_headers,
  subdir : 'pulsecore/modules/meego'
)

libmeego_common_sailfishos_headers = [
  'include/sailfishos/shared-data.h',
]

install_headers(
  'include/sailfishos/defines.h',
  subdir : 'pulsecore/modules/sailfishos'
)

libmeego_common_inc = include_directories('include', 'include/meego')

libmeego_common_deps = [alsa_dep, dbus_dep, pulsecore_dep]

libmeego_common = library('meego-common',
  libmeego_common_sources,
  include_directories : [configinc, libmeego_common_inc],
  link_args : '-lm',
  c_args : [pa_c_args],
  install : true,
  install_dir : modlibexecdir,
  install_rpath : rpath_dirs,
  dependencies : libmeego_common_deps,
)

meego_common_dep = declare_dependency(
  link_with : libmeego_common,
  compile_args : pa_c_args,
  dependencies : libmeego_common_deps,
  include_directories : [configinc, libmeego_common_inc],
)

check_common = executable('check_common',
  'tests.c',
  include_directories : [configinc],
  c_args : [pa_c_args],
  dependencies : [check_dep, meego_common_dep],
)

# pkgconfig
pc_cdata = configuration_data()

pc_cdata.set('prefix', get_option('prefix'))
pc_cdata.set('libdir', libdir)
pc_cdata.set('libexecdir', get_option('libexecdir'))
pc_cdata.set('PA_MAJORMINOR', pa_version_major_minor)
pc_cdata.set('PA_MODULE_VERSION', pa_version_module)

configure_file(
  input : 'libmeego-common.pc.in',
  output : 'libmeego-common.pc',
  configuration : pc_cdata,
  install_dir : join_paths(libdir, 'pkgconfig')
)
