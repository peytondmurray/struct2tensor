py.install_sources(
  [
    '__init__.py',
    'file_descriptor_set.py',
    'file_descriptor_set_test.py',
    'gen_decode_proto_map_op.py',
    'gen_decode_proto_sparse.py',
    'gen_equi_join_any_indices.py',
    'gen_equi_join_indices.py',
    'gen_parquet_dataset.py',
    'gen_run_length_before.py',
    'struct2tensor_ops.py',
    'struct2tensor_ops_test.py',
  ],
  subdir: 'struct2tensor/ops',
  pure: false
)

py.extension_module(
    '_parquet_dataset_op',
    srcs: [
      'parquet_dataset_op.cc',
    ]
    install: true,
    subdir: 'versioned_hdf5',
)
