project('libwmf test', 'c')

libwmf_dep = dependency('libwmf', version : '>= 0.2.8')
libwmf_ver = libwmf_dep.version()
assert(libwmf_ver.split('.').length() > 1, 'libwmf version is "@0@"'.format(libwmf_ver))
message('libwmf version is "@0@"'.format(libwmf_ver))
e = executable('libwmf_prog', 'libwmf_prog.c', dependencies : libwmf_dep)

test('libwmftest', e)

# Test using the method keyword:

dependency('libwmf', method : 'config-tool')
dependency('libwmf', method : 'libwmf-config')
