package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

cc_library(
  name = "cbits",
  hdrs = glob(["include/*.h", "internal/*"]),
  #data = ["internal/unbox-tuple-instances"],
  #copts = ["-Iexternal/text/include"],
)


haskell_library(
  name = 'vector',
  version = "0.12.0.1",
  srcs = glob(['Control/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  #compiler_flags = ["-XCPP", "-XMultiParamTypeClasses", "-XFunctionalDependencies", "-XFlexibleInstances", "-Wall -fno-warn-unused-imports -fno-warn-warnings-deprecations -Wcompat -Wnoncanonical-monad-instances -Wnoncanonical-monadfail-instances"],
  prebuilt_dependencies = [
    "base", "deepseq", "ghc-prim", "semigroups"
  ],
  deps = [
    ":cbits",
    "@primitive//:primitive"
  ]

)

