workspace(name = "hello")

new_http_archive(
    name = "safe",
    build_file_content = """

package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'safe',
  srcs = glob(['Safe/*.hs', 'Safe.hs']),
  prebuilt_dependencies = [
    "base"
  ],
  deps = [

  ]
)
""",
    strip_prefix = "safe-0.3.15",
    urls = [
        "https://hackage.haskell.org/package/safe-0.3.15/safe-0.3.15.tar.gz"
    ],
)


new_http_archive(
    name = "random",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'random',
  srcs = glob(['System/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  compiler_flags = ["-XCPP"],
  prebuilt_dependencies = [
    "base","time"
  ],
  deps = [

  ]
)
""",
    strip_prefix = "random-1.1",
    urls = [
        "https://hackage.haskell.org/package/random-1.1/random-1.1.tar.gz"
    ],
)

new_http_archive(
    name = "integer_logarithms",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'integer-logarithms',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  src_strip_prefix = "src",
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "integer-gmp","ghc-prim","base","array"
  ],
  deps = [

  ]
)
""",
    strip_prefix = "integer-logarithms-1.0.2",
    urls = [
        "https://hackage.haskell.org/package/integer-logarithms-1.0.2/integer-logarithms-1.0.2.tar.gz"
    ],
)
new_http_archive(
    name = "attoparsec",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'attoparsec',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "deepseq","array","bytestring","transformers","base","containers"
  ],
  deps = [
    "@scientific//:scientific",
    "@text//:text"
  ]
)
""",
    strip_prefix = "attoparsec-0.13.2.0",
    urls = [
        "https://hackage.haskell.org/package/attoparsec-0.13.2.0/attoparsec-0.13.2.0.tar.gz"
    ],
)

new_http_archive(
    name = "th_abstraction",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'th-abstraction',
  src_strip_prefix = "src",
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "template-haskell","ghc-prim","base","containers"
  ],
  deps = [

  ]
)
""",
    strip_prefix = "th-abstraction-0.2.6.0",
    urls = [
        "https://hackage.haskell.org/package/th-abstraction-0.2.6.0/th-abstraction-0.2.6.0.tar.gz"
    ],
)


new_http_archive(
    name = "uuid_types",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'uuid-types',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "deepseq","bytestring","base","binary"
  ],
  deps = [
    "@hashable//:hashable",
    "@text//:text",
    "@random//:random"
  ]
)
""",
    strip_prefix = "uuid-types-1.0.3",
    urls = [
        "https://hackage.haskell.org/package/uuid-types-1.0.3/uuid-types-1.0.3.tar.gz"
    ],
)

new_http_archive(
    name = "base_compat",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'base-compat',
  src_strip_prefix = "src",
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "unix","base"
  ],
  deps = [

  ]
)
""",
    strip_prefix = "base-compat-0.9.3",
    urls = [
        "https://hackage.haskell.org/package/base-compat-0.9.3/base-compat-0.9.3.tar.gz"
    ],
)


new_http_archive(
    name = "scientific",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'scientific',
  src_strip_prefix = "src",
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  prebuilt_dependencies = [
    "integer-gmp","deepseq","binary","bytestring","base","containers"
  ],
  deps = [
    "@integer_logarithms//:integer-logarithms",
    "@hashable//:hashable",
    "@text//:text",
    "@primitive//:primitive"
  ]
)
""",
    strip_prefix = "scientific-0.3.5.2",
    urls = [
        "https://hackage.haskell.org/package/scientific-0.3.5.2/scientific-0.3.5.2.tar.gz"
    ],
)

new_http_archive(
    name = "time_locale_compat",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'time-locale-compat',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  src_strip_prefix = "src",
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "base","time"
  ],
  deps = [

  ]
)
""",
    strip_prefix = "time-locale-compat-0.1.1.3",
    urls = [
        "https://hackage.haskell.org/package/time-locale-compat-0.1.1.3/time-locale-compat-0.1.1.3.tar.gz"
    ],
)

new_http_archive(
    name = "dlist",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'dlist',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "deepseq","base"
  ],
  deps = [

  ]
)
""",
    strip_prefix = "dlist-0.8.0.3",
    urls = [
        "https://hackage.haskell.org/package/dlist-0.8.0.3/dlist-0.8.0.3.tar.gz"
    ],
)

new_http_archive(
    name = "aeson",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

cc_library(
  name = "cbits",
  srcs = ["cbits/unescape_string.c"],
  hdrs = glob(["include/*.h"]),
  copts = ["-Iexternal/aeson/include"],
)

haskell_library(
  name = 'aeson',
  srcs = glob(['src/**/*.hs', 'attoparsec-iso8601/**/*.hs' ,'Data/**/*.hs', 'pure/**/*.hs']),
  prebuilt_dependencies = [
    "deepseq","template-haskell","time","bytestring","ghc-prim","base","containers"
  ],
  compiler_flags = [],
  deps = [
    ":cbits",
    "@dlist//:dlist",
    "@vector//:vector",
    "@text//:text",
    "@scientific//:scientific",
    "@hashable//:hashable",
    "@uuid_types//:uuid-types",
    "@unordered_containers//:unordered-containers",
    "@tagged//:tagged",
    "@base_compat//:base-compat",
    "@th_abstraction//:th-abstraction",
    "@time_locale_compat//:time-locale-compat",
    "@attoparsec//:attoparsec",
  ]
)
""",
    strip_prefix = "aeson-1.2.3.0",
    urls = [
        "https://hackage.haskell.org/package/aeson-1.2.3.0/aeson-1.2.3.0.tar.gz"
    ],
)


new_http_archive(
    name = "bytestring_builder",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'bytestring_builder',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "deepseq","base","bytestring"
  ],
  deps = [

  ]
)
""",
    strip_prefix = "bytestring-builder-0.10.8.1.0",
    urls = [
        "https://hackage.haskell.org/package/bytestring-builder-0.10.8.1.0/bytestring-builder-0.10.8.1.0.tar.gz"
    ],
)

new_http_archive(
    name = "unordered_containers",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'unordered-containers',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "deepseq","base"
  ],
  deps = [
    "@hashable//:hashable"
  ]
)
""",
    strip_prefix = "unordered-containers-0.2.8.0",
    urls = [
        "https://hackage.haskell.org/package/unordered-containers-0.2.8.0/unordered-containers-0.2.8.0.tar.gz"
    ],
)
new_http_archive(
    name = "tagged",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

haskell_library(
  name = 'tagged',
  src_strip_prefix = "src",
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "deepseq","template-haskell","transformers","base"
  ],
  deps = [
    #"@transformers_compat//:transformers_compat"
  ]
)
""",
    strip_prefix = "tagged-0.8.5",
    urls = [
        "https://hackage.haskell.org/package/tagged-0.8.5/tagged-0.8.5.tar.gz"
    ],
)
new_http_archive(
    name = "protolude",
    build_file_content = """

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
    "base","bytestring","array","ghc-prim","deepseq","containers","transformers",
  ],
  deps = [
    "@safe//:safe",
    "@async//:async",
    "@text//:text",
    "@mtl//:mtl",
    "@stm//:stm",
    "@semigroups//:semigroups",
    "@hashable//:hashable"
  ]
)
""",
    strip_prefix = "protolude-0.2.1",
    urls = [
        "https://hackage.haskell.org/package/protolude-0.2.1/protolude-0.2.1.tar.gz"
    ],
)



new_http_archive(
    name = "hashable",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

load(
  "@io_tweag_rules_haskell//haskell:haskell.bzl",
  "haskell_library","haskell_binary"
)

cc_library(
  name = "fnv",
  srcs = ["cbits/fnv.c"],
)

haskell_library(
  name = 'hashable',
  srcs = glob(['src/**/*.hs', 'lib/**/*.hs' ,'Data/**/*.hs']),
  version = "1.2.6.1",
  compiler_flags = ["-XTypeSynonymInstances", "-DGENERICS"],
  # c_sources = glob(['cbits/**/*.c']),
  prebuilt_dependencies = [
    "base","ghc-prim","integer-gmp","bytestring", "deepseq"
  ],
  deps = [
    ":fnv",
    "@text//:text",
  ]
)
""",
    strip_prefix = "hashable-1.2.6.1",
    urls = [
        "https://hackage.haskell.org/package/hashable-1.2.6.1/hashable-1.2.6.1.tar.gz"
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
    name = "semigroups",
    build_file = "semigroups.BUILD",
    strip_prefix = "semigroups-0.18.3",
    urls = [
        "https://hackage.haskell.org/package/semigroups-0.18.3/semigroups-0.18.3.tar.gz"
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
  strip_prefix = "rules_haskell-master",
  urls = ["https://github.com/tweag/rules_haskell/archive/master.tar.gz"]
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

#new_http_archive(
    #name = "ghc_bindist",
    #urls = [
      #"https://downloads.haskell.org/~ghc/8.2.2/ghc-8.2.2-x86_64-deb8-linux.tar.xz",
    #],
    #strip_prefix = "ghc-8.2.2",
    #build_file_content = """
#package(default_visibility = ["//visibility:public"])

#genrule(
      #name = "ghc_bindist",
      #outs = glob(["out/**/*"]),
      #cmd = "./configuire --prefix=`pwd`/out > $@",
#)

#"""
#)
register_toolchains(
  "//:ghc_toolchain",
)


