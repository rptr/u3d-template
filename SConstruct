VariantDir('build', 'src')

urho = ARGUMENTS.get('urho', '/home/rpj/a/repos/Urho3D-1.7')

env = Environment(CPPPATH = urho+'/include:'+urho+'/include/Urho3D/ThirdParty')

cxxflags = "-std=c++11 -msse3 -ggdb -g3"
lib_path = [urho + '/lib', '/lib/x86_64-linux-gnu']
libs = ['libUrho3D', 'libSDL2', 'libdl', 'libpthread', 'libGLEW', 'libGL']

cli_files = [Glob('src/*.cpp')]

demo = env.Program('demo',
                    cli_files, 
                    LIBS=libs, 
                    LIBPATH=lib_path, 
                    CXXFLAGS=cxxflags)

