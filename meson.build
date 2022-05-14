project('gp-demo', 'c',
    default_options : [
        'c_std=c99',
        'c_args=-Wall -Werror -pedantic -D_FORTIFY_SOURCE=2',
        'b_ndebug=if-release'])

# make sure gnuplot is available
gnuplot = find_program('gnuplot', required : true)

cc = meson.get_compiler('c')
m_dep = cc.find_library('m', required : false)

gp_test = executable('gp_test',
    'gp_test.c',
    dependencies : m_dep)
