from building import *

# get current directory
cwd     = GetCurrentDir()
# The set of source files associated with this SConscript file.
src     = Glob('src/*.c')
src    += Glob('port/*.c')

path    = [cwd + '/inc']

if GetDepend(['PKG_ELOG_ENABLE_PLUGIN_FLASH']):
    src    += Glob('plugins/flash/*.c')
    path   += [cwd + '/plugins/flash']

group = DefineGroup('EasyLogger', src, depend = [''], CPPPATH = path)

Return('group')
