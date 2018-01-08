package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'hashable',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "base","ghc-prim","text","integer-gmp","bytestring"
  ],
  deps = [

  ]
)

