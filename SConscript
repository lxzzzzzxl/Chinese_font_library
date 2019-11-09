# RT-Thread building script for bridge
Import('RTT_ROOT')
Import('rtconfig')
import os
from building import *

cwd = GetCurrentDir()
objs = []
list = os.listdir(cwd)

if GetDepend('PKG_USING_CHINESE_FONT_LIBRARY'):
    for d in list:
        path = os.path.join(cwd, d)
        if os.path.isfile(os.path.join(path, 'SConscript')):
            objs = objs + SConscript(os.path.join(d, 'SConscript'))

Return('objs')