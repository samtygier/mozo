config_py = configuration_data()
config_py.set('prefix', prefix)
config_py.set('datadir', datadir)
config_py.set('pkgdatadir', join_paths(datadir, meson.project_name()))
config_py.set('PACKAGE', meson.project_name())
config_py.set('VERSION', meson.project_version())
config_py.set('GETTEXT_PACKAGE', meson.project_name())

config = configure_file(
  input: 'config.py.in',
  output: 'config.py',
  configuration: config_py,
  )

mozo_sources = [
'__init__.py',
'MainWindow.py',
'MenuEditor.py',
'util.py',
]

python3.install_sources(config, mozo_sources)
