package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

cc_library(
  name = "fnv",
  srcs = ["cbits/fnv.c"],
)

haskell_library(
  name = 'hashable',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  version = "1.2.6.1",
  compiler_flags = ["-XTypeSynonymInstances", "-DGENERICS"],
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "base","ghc-prim","integer-gmp","bytestring"
  ],
  deps = [
    ":fnv",
    "@text//:text",
  ]
)

