libgstdroid_sources = [
  'plugin.c',
]

libgstdroid_headers = [
  'plugin.h',
]

subdir('droidcodec')
subdir('droideglsink')
subdir('droidcamsrc')

libgstdroid = library('gstdroid',
  libgstdroid_sources + libgstdroid_headers,
  c_args : gstdroid_args + ['-DGST_USE_UNSTABLE_API'],
  include_directories : [configinc, libsinc, 'droidcamsrc', 'droidcodec', 'droideglsink'],
  dependencies : [ gst_dep, gstdroidcamsrc_dep, gstdroidcodec_dep, gstdroideglsink_dep, droidmedia_dep ],
  install : true,
  install_dir : plugins_install_dir,
)

plugins = [gstdroid]
