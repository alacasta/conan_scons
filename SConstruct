import os

# Import Conans
from conans.client.conan_api import ConanAPIV1 as conan_api
from conans import __version__ as conan_version

conan, _, _ = conan_api.factory()

build_directory = os.path.join(os.getcwd(), "build")
if not os.path.exists(build_directory):
    os.makedirs(build_directory)

src_directory = os.path.join(os.getcwd(), "src")
build_hello_directory = os.path.join(src_directory, "hello.c")

conanfile_path = os.path.join(os.getcwd(), "conanfile.txt")

conan.install(conanfile_path,\
        generators=["scons"],\
        install_folder=build_directory)


# SConstruct
env = Environment()

conan = SConscript('{}/SConscript_conan'.format(build_directory))
flags = conan["conan"]
env.MergeFlags(flags)

VariantDir(build_directory, src_directory)
hello = Program(build_hello_directory)