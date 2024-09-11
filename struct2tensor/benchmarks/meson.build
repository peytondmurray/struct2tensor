py.install_sources(
  [
      'ops_benchmark.py',
      'struct2tensor_benchmark.py',
      'struct2tensor_benchmark_util.py',
  ],
  subdir: 'struct2tensor/benchmarks',
  pure: false
)


proto_files = [
  'benchmark.proto',
]

# Generate cpp and python code
custom_target(
  command: [protoc, '--proto_path=@CURRENT_SOURCE_DIR@', '--cpp_out=@OUTDIR@', '--python_out=@OUTDIR@', '@INPUT@'],
  input: proto_files,
  output: ['@BASENAME@.pb.cc', '@BASENAME@.pb.h', '@BASENAME@_pb2.py'],
  build_by_default: true,
)
