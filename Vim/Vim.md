# Vim Setting

## Youcompleteme

### Installation
- Vundle
- Compile
### YCM configure file

    vim ~/.vim/ycm_extra_conf.py

Content of ycm_extra_conf.py

    import os
    import ycm_core

    flags = [
        '-Wall',
        '-Wextra',
        '-Werror',
        '-Wno-long-long',
        '-Wno-variadic-macros',
        '-fexceptions',
        '-DNDEBUG',
        '-std=c++11',
        '-x',
        'c++',
        '-I',
        '/usr/include',
        '-isystem',
        '/usr/lib/gcc/x86_64-linux-gnu/5/include',
        '-isystem',
        '/usr/include/x86_64-linux-gnu',
        '-isystem'
        '/usr/include/c++/5',
        '-isystem',
        '/usr/include/c++/5/bits'
    ]

    SOURCE_EXTENSIONS = [ '.cpp', '.cxx', '.cc', '.c', ]

    def FlagsForFile( filename, **kwargs ):
    return {
        'flags': flags,
        'do_cache': True
    }

Add path of ycm_extra_conf.py and YCM configure in vimrc

    vim ~/.vimrc

    # Add content below into vimrc
    let g:ycm_global_ycm_extra_conf='~/.vim/ycm_extra_conf.py'
    let g:ycm_confirm_extra_conf = 0

    let g:ycm_semantic_triggers =  {
              \ 'c,cpp,python,java,go,erlang,perl': ['re!\w{2}'],
              \ 'cs,lua,javascript': ['re!\w{2}'],
              \ }
    
