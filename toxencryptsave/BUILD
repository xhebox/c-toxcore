load("//tools:no_undefined.bzl", "cc_library")

filegroup(
    name = "public_headers",
    srcs = ["toxencryptsave.h"],
    visibility = ["//c-toxcore:__pkg__"],
)

cc_library(
    name = "defines",
    hdrs = ["defines.h"],
    visibility = ["//c-toxcore/toxcore:__pkg__"],
)

cc_library(
    name = "toxencryptsave",
    srcs = ["toxencryptsave.c"],
    hdrs = ["toxencryptsave.h"],
    visibility = ["//c-toxcore:__subpackages__"],
    deps = [
        ":defines",
        "//c-toxcore/toxcore:crypto_core",
    ],
)

cc_library(
    name = "monolith",
    hdrs = glob([
        "*.c",
        "*.h",
    ]),
    visibility = ["//c-toxcore/other:__pkg__"],
    deps = ["//c-toxcore/toxcore:crypto_core"],
)
