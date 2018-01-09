package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'protolude',
  src_strip_prefix = "src",
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),

  # c_sources = glob(['cbits/**/*.c']),
  compiler_flags = ["-XMultiParamTypeClasses","-XFlexibleContexts","-XOverloadedStrings","-XNoImplicitPrelude"],
  prebuilt_dependencies = [
    "base","bytestring","array","ghc-prim","deepseq","containers","stm","transformers",
    "mtl"
  ],
  deps = [
    "@safe//:safe",
    "@async//:async",
    "@text//:text",

    "@hashable//:hashable"
  ]
)

