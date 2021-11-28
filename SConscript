from building import *

src   = ['rt_vsnprintf.c']
CPPDEFINES = []

if GetDepend('RT_VSNPRINTF_FULL_REPLACING_SPRINTF'):
    CPPDEFINES += ['sprintf=rt_sprintf']
if GetDepend('RT_VSNPRINTF_FULL_REPLACING_SNPRINTF'):
    CPPDEFINES += ['snprintf=rt_snprintf']
if GetDepend('RT_VSNPRINTF_FULL_REPLACING_PRINTF'):
    CPPDEFINES += ['printf=rt_kprintf']

group = DefineGroup('Kernel', src, depend = ['PKG_USING_RT_VSNPRINTF_FULL'], CPPDEFINES = CPPDEFINES)
Return('group')
