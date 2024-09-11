subdir('parquet')

shared_library(
  'run_length_before_op_dynamic',
  [
    'run_length_before_op.cc'
  ]
)

py.extension_module(
  '_main',
  srcs,
  install: true,
  subdir: 'stringdtype',
  include_directories: includes,
  dependencies: [np_dep, npymath_lib]
)
