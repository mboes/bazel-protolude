
package(default_visibility = ["//visibility:public"])
load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'semigroups',
  version = "2.2.1",
  src_strip_prefix = "src",
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  compiler_flags = ["-XCPP", "-XMultiParamTypeClasses", "-XFunctionalDependencies", "-XFlexibleInstances", "-Wall -fno-warn-unused-imports -fno-warn-warnings-deprecations -Wcompat -Wnoncanonical-monad-instances -Wnoncanonical-monadfail-instances"],
  prebuilt_dependencies = [
    "base", "transformers"
  ],
  deps = [
  ]
)

