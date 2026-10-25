load("@emb_toolchain//platforms/c2000/toolchain:cc_binary_c2000.bzl", "cc_binary_c2000")

# Application specific FreeRTOS configuration
# Only allowed to be included within os/include
cc_library(
    name = "app_defines",
    hdrs = [
        "appDefines.h"
    ],
    includes = ["."],
    visibility = ["//applications/tif2838:__subpackages__"],
)

cc_binary_c2000(
    name = "app",
    srcs = [
        "codestart.asm",
        "main.c",
    ],
    deps = [
        ":app_defines",
        "@emb_platform//c2000/mcal/f28p65/code:mcal_f28p65x",
        "//applications/tif2838/public:public_types_h",
        "//applications/tif2838/swe/app/tasks:tasks",
        "//applications/tif2838/units:units_app",
    ],
    # Declare addation linker inputs - needed for linkopts
    additional_linker_inputs = [
        "//applications/tif2838/swe/linker:linker_cmd_app",
    ],
    # Linker options
    linkopts = [
        "--library=$(location //applications/tif2838/swe/linker:linker_cmd_app)",
    ],
    visibility = ["//applications/tif2838:__subpackages__"],
)

cc_binary_c2000(
    name = "app_c2000",
    srcs = [
        ":app",
    ],
)
