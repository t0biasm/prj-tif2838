filegroup(
    name = "srcs",
    srcs = glob(["*.c"]),
    visibility = ["//applications/tif2838:__subpackages__"],
)

filegroup(
    name = "hdrs",
    srcs = glob(["*.h"]),
    visibility = ["//applications/tif2838:__subpackages__"],
)

cc_library(
    name = "drvLedCtrl",
    srcs = [":srcs"],
    hdrs = [":hdrs"],
    deps = [
        "@emb_platform//c2000/mcal/f28p65/code:mcal_f28p65x",
    ],
    includes = ["."],
    visibility = ["//applications/tif2838:__subpackages__"],
)
