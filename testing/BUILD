load("//tools:no_undefined.bzl", "cc_library")

cc_library(
    name = "misc_tools",
    hdrs = [
        "misc_tools.c",
    ],
    visibility = ["//c-toxcore:__subpackages__"],
)

cc_binary(
    name = "DHT_test",
    srcs = ["DHT_test.c"],
    deps = [
        ":misc_tools",
        "//c-toxcore/toxcore",
    ],
)

cc_binary(
    name = "Messenger_test",
    srcs = ["Messenger_test.c"],
    deps = [
        ":misc_tools",
        "//c-toxcore/toxcore",
    ],
)

cc_binary(
    name = "av_test",
    srcs = ["av_test.c"],
    linkopts = [
        "-lopencv_highgui",
        "-lopencv_core",
    ],
    deps = [
        "//c-toxcore/toxav",
        "//c-toxcore/toxav:monolith",
        "//c-toxcore/toxcore",
        "@portaudio",
        "@sndfile",
    ],
)

cc_binary(
    name = "irc_syncbot",
    srcs = ["irc_syncbot.c"],
    deps = [
        ":misc_tools",
        "//c-toxcore/toxcore",
    ],
)

cc_binary(
    name = "tox_shell",
    srcs = ["tox_shell.c"],
    linkopts = ["-lutil"],
    deps = [
        ":misc_tools",
        "//c-toxcore/toxcore",
    ],
)

cc_binary(
    name = "tox_sync",
    srcs = ["tox_sync.c"],
    deps = [
        ":misc_tools",
        "//c-toxcore/toxcore",
    ],
)
