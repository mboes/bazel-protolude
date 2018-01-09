package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

cc_library(
  name = "cbits",
  srcs = ["cbits/cbits.c"],
  hdrs = ["include/text_cbits.h"],
  copts = ["-Iexternal/text/include"],
)

haskell_library(
  name = 'text',
  srcs = glob(['Control/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  version = "1.2.2.2",
  compiler_flags = ["-DINTEGER_GMP", "-DHAVE_DEEPSEQ"],
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "base", "deepseq", "bytestring", "ghc-prim", "binary", "array", "integer-gmp"
  ],
  deps = [
    ":cbits"
  ]
)
