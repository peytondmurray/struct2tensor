py.install_sources(
  [
    '__init__.py',
    'calculate.py',
    'calculate_options.py',
    'calculate_test.py',
    'calculate_with_source_paths.py',
    'calculate_with_source_paths_test.py',
    'create_expression.py',
    'create_expression_test.py',
    'expression.py',
    'expression_add.py',
    'expression_add_test.py',
    'expression_test.py',
    'path.py',
    'path_test.py',
    'prensor.py',
    'prensor_test.py',
    'prensor_to_structured_tensor.py',
    'prensor_to_structured_tensor_test.py',
    'prensor_util.py',
    'prensor_value.py',
    'prensor_value_test.py',
    'struct2tensor_module_test.py',
    'structured_tensor_to_prensor.py',
    'structured_tensor_to_prensor_test.py',
    'version.py',
  ],
  subdir: 'struct2tensor',
  pure: false
)

subdir('benchmarks')
subdir('expression_impl')
subdir('kernels')
subdir('ops')
subdir('proto')
subdir('test')
subdir('testdata')
subdir('tools')


# Ops
py.extension_module(
  '_decode_proto_map_op',
  srcs: [
    'ops/parquet_dataset_op.cc',
  ],
  install: true,
  subdir: 'struct2tensor/ops',
)

# depends on tensorflow/core:framework
py.extension_module(
  '_decode_proto_sparse_op',
  srcs: [
    'ops/decode_proto_sparse_op.cc',
  ],
  install: true,
  subdir: 'struct2tensor/ops',
  dependencies: [tf_dep],
)

# depends on equi_join_any_indices_op_dynamic
py.extension_module(
  '_equi_join_any_indices_op',
  srcs: [
    'ops/equi_join_any_indices_op.cc',
  ],
  install: true,
  subdir: 'struct2tensor/ops',
)


# depends on tensorflow/core:framework
py.extension_module(
  '_equi_join_indices_op',
  srcs: [
    'ops/equi_join_indices_op.cc',
  ],
  install: true,
  subdir: 'struct2tensor/ops',
  dependencies: [tf_dep],
)

# depends on
# tensorflow/core:dataset_ops_op_lib
# tensorflow/core:framework
py.extension_module(
  '_parquet_dataset_op',
  srcs: [
    'ops/parquet_dataset_op.cc',
  ],
  install: true,
  subdir: 'struct2tensor/ops',
  dependencies: [tf_dep],
)

# depends on
# run_length_before_op_dynamic
py.extension_module(
  '_run_length_before_op',
  srcs: [
    'ops/run_length_before_op.cc',
  ],
  install: true,
  subdir: 'struct2tensor/ops',
)
