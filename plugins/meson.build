# Keep the autotools convention for shared module suffix because GModule
# depends on it: https://gitlab.gnome.org/GNOME/glib/issues/520
module_suffix = []
if host_machine.system() == 'darwin'
  module_suffix = 'so'
endif

msgfmt_plugin_cmd = [
  find_program('msgfmt'),
  '--desktop',
  '--keyword=Name',
  '--keyword=Description',
  '--template=@INPUT@',
  '-d', join_paths(srcdir, 'po'),
  '--output=@OUTPUT@'
]

if build_checkupdate_plugin
  subdir('checkupdate')
endif

subdir('docinfo')
subdir('externaltools')
subdir('filebrowser')
subdir('modelines')
subdir('pythonconsole')
subdir('quickhighlight')
subdir('quickopen')
subdir('snippets')
subdir('sort')
subdir('spell')
subdir('time')
