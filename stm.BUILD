package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'stm',
  version = "2.4.4.1",
  srcs = glob(['Control/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  #compiler_flags = ["-XCPP", "-XMultiParamTypeClasses", "-XDeriveDataTypeable", "-XFlexibleInstances", "-XMagicHash"],
  prebuilt_dependencies = [
    "base", "transformers", "array"
  ],
  deps = [
  ]
)

