workspace(name = "hello")

new_http_archive(
    name = "safe",
    build_file = "safe.BUILD",
    strip_prefix = "safe-0.3.15",
    urls = [
        "https://hackage.haskell.org/package/safe-0.3.15/safe-0.3.15.tar.gz"
    ],
)

new_http_archive(
    name = "protolude",
    build_file = "protolude.BUILD",
    strip_prefix = "protolude-0.2",
    urls = [
        "https://hackage.haskell.org/package/protolude-0.2/protolude-0.2.tar.gz"
    ],
)

new_http_archive(
    name = "mtl_compat",
    build_file = "mtl_compat.BUILD",
    strip_prefix = "mtl-compat-0.2.1.3",
    urls = [
        "https://hackage.haskell.org/package/mtl-compat-0.2.1.3/mtl-compat-0.2.1.3.tar.gz"
    ],
)


new_http_archive(
    name = "hashable",
    build_file = "hashable.BUILD",
    strip_prefix = "hashable-1.2.4.0",
    urls = [
        "https://hackage.haskell.org/package/hashable-1.2.4.0/hashable-1.2.4.0.tar.gz"
    ],
)

new_http_archive(
    name = "async",
    build_file = "async.BUILD",
    strip_prefix = "async-2.1.1.1",
    urls = [
        "https://hackage.haskell.org/package/async-2.1.1.1/async-2.1.1.1.tar.gz"
    ],
)

new_http_archive(
    name = "stm",
    build_file = "stm.BUILD",
    strip_prefix = "stm-2.4.4.1",
    urls = [
        "https://hackage.haskell.org/package/stm-2.4.4.1/stm-2.4.4.1.tar.gz"
    ],
)

new_http_archive(
    name = "mtl",
    build_file = "mtl.BUILD",
    strip_prefix = "mtl-2.2.1",
    urls = [
        "https://hackage.haskell.org/package/mtl-2.2.1/mtl-2.2.1.tar.gz"
    ],
)

new_http_archive(
    name = "text",
    build_file = "text.BUILD",
    strip_prefix = "text-1.2.2.2",
    urls = [
        "https://hackage.haskell.org/package/text-1.2.2.2/text-1.2.2.2.tar.gz"
    ],
)



new_http_archive(
    name = "vector",
    build_file = "vector.BUILD",
    strip_prefix = "vector-0.12.0.1",
    urls = [
        "https://hackage.haskell.org/package/vector-0.12.0.1/vector-0.12.0.1.tar.gz"
    ],
)

new_http_archive(
    name = "primitive",
    build_file = "primitive.BUILD",
    strip_prefix = "primitive-0.6.2.0",
    urls = [
        "https://hackage.haskell.org/package/primitive-0.6.2.0/primitive-0.6.2.0.tar.gz"
    ],
)


http_archive(
  name = "io_tweag_rules_haskell",
  strip_prefix = "rules_haskell-0.2",
  urls = ["https://github.com/tweag/rules_haskell/archive/v0.2.tar.gz"]
)

#local_repository(
    #name = "io_tweag_rules_haskell",
    #path = "/home/redacted/src/rules_haskell",
#)
load("@io_tweag_rules_haskell//haskell:repositories.bzl", "haskell_repositories")
haskell_repositories()

new_local_repository(
  name = "ghc",
  path = "/usr/",
  build_file_content = """
package(default_visibility = ["//visibility:public"])
filegroup(
  name = "bin",
  srcs = glob([
    "bin/ghc*",
    "bin/hsc2hs",
    "bin/gcc",
    "bin/as",
    "bin/ld.gold",
    "bin/dirname",
    "bin/realpath",
    "lib/gcc/*/*/cc1",
  ])
)
cc_library(
  name = "threaded-rts",
  srcs = glob(["lib/ghc-*/rts/libHSrts_thr-ghc*.so"]),
  hdrs = glob(["lib/ghc-*/include/**/*.h"]),
  strip_include_prefix = glob(["lib/ghc-*/include"], exclude_directories=0)[0],
)

"""
)

register_toolchains(
  "//:ghc_toolchain",
)


