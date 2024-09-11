project(
  'struct2tensor',
  'cpp',
  version: '4.00',
)

py = import('python').find_installation(pure: false)

protobuf_dep = dependency(
  'protobuf',
  modules: ['protobuf::protoc'],
  version: '>=27',
)
absl_dep = dependency('absl', modules: ['absl::optional'])
pybind11_dep = dependency('pybind11', version: '>=2.11.1')
protoc = find_program('protoc', required : true)
protobuf_dep = dependency('protobuf', version: '>=3.21.9', required: true)

# Find the tensorflow directory; declare the include directory as a dependency
incdir_tf = run_command(py,
  [
    '-c',
    'import tensorflow.sysconfig; print(tensorflow.sysconfig.get_include())'
  ],
  check: true
).stdout().strip()
inc_tf = include_directories(incdir_tf)
tf_dep = declare_dependency(include_directories: inc_tf)


# includes = include_directories(
#   [
#     incdir_tf,
#     # 'stringdtype/src'
#   ]
# )

subdir('struct2tensor')


# py.extension_module(
#   '_main',
#   srcs,
#   install: true,
#   subdir: 'stringdtype',
#   include_directories: includes,
#   dependencies: [np_dep, npymath_lib]
# )
