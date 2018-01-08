
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'mtl_compat',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "base","mtl"
  ],
  deps = [

  ]
)

