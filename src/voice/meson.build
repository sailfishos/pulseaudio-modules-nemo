meego_voice_sources = [
  'module-meego-voice.c',
  'voice-aep-sink-input.c',
  'voice-hw-sink-input.c',
  'voice-hw-source-output.c',
  'voice-mainloop-handler.c',
  'voice-raw-sink.c',
  'voice-raw-source.c',
  'voice-util.c',
  'voice-voip-sink.c',
  'voice-voip-source.c',
]

meego_voice = library('module-meego-voice',
  meego_voice_sources,
  c_args : [pa_c_args, '-DPA_MODULE_NAME=module_meego_voice'],
  install : true,
  install_dir : modlibexecdir,
  install_rpath : rpath_dirs,
  dependencies : [meego_common_dep],
  name_prefix : ''
)
