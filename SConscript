from building import *
Import('rtconfig')

src   = []
cwd   = GetCurrentDir()

if GetDepend('PKG_DF220_USING_SENSOR_V1'):
   src += Glob('mira_df220_sensor_v1.c')

# add df220 src files.
src += Glob('libraries/df220.c')

# add df220 include path.
path  = [cwd, cwd + '/libraries']

# add src and include to group.
group = DefineGroup('df220', src, depend = ['PKG_USING_DF220'], CPPPATH = path)

Return('group')
