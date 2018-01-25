package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_binary",
  "haskell_toolchain",
)

haskell_toolchain(
  name = "ghc_toolchain",
  version = "8.2.2",
  tools = "@ghc//:bin",
)

haskell_binary(
  name = "hello",
  srcs = ['Main.hs'],
  #compiler_flags = [ "-XNoImplicitPrelude"],
  prebuilt_dependencies = ["base", "bytestring"],
  deps = ["@vector//:vector", "@semigroups//:semigroups", "@protolude//:protolude", "@primitive//:primitive" ],
)

