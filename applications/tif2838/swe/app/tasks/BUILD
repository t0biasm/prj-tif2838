cc_library(
    name = "tasks",
    srcs = glob(["*.c"]),
    hdrs = glob(
        ["*.h"], 
        exclude = ["FreeRTOSConfig.h"],
    ),
    deps = [
        "//applications/tif2838/public:public_types_h",
        "//applications/tif2838/swe/app:app_defines",
        "//applications/tif2838/units/drvLedCtrl/code:drvLedCtrl",
        "@emb_platform//c2000/freertos:free_rtos_c28x_app",
    ],
    includes = ["."],
    visibility = ["//applications/tif2838/swe/app:__subpackages__"],
)

cc_library(
    name = "free_rtos_app_config",
    hdrs = [
        "FreeRTOSConfig.h"
    ],
    includes = ["."],
    visibility = ["//visibility:public"],
)
