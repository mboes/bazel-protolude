
package(default_visibility = ["//visibility:public"])
load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)


cc_library(
  name = "cbits",
  srcs = glob(["cbits/*.c"]),
  hdrs = glob(["cbits/*.h"]),
  deps = ["@ghc//:threaded-rts"],
  copts = ["-fomit-frame-pointer"]
)

haskell_library(
  name = 'primitive',
  version = "0.6.2.0",
  srcs = glob(['Control/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  prebuilt_dependencies = [
    "base", "transformers", "ghc-prim"
  ],
  deps = [
    ":cbits"
  ]
)

