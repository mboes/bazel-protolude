package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'protolude',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "base","bytestring","mtl","text","array","ghc-prim","deepseq","containers","stm","transformers"
  ],
  deps = [
    "@safe//:safe",
    "@mtl_compat//:mtl_compat",
    "@async//:async",
    "@hashable//:hashable"
  ]
)

