cc_library(
    name = "sysHwCfg_app",
    srcs = glob(["*.c"]),
    hdrs = glob(["*.h"]),
    deps = [
        "@emb_platform//c2000/mcal/f28p65/code:mcal_f28p65x",
        "//applications/tif2838/public:public_types_h",
        "//applications/tif2838/swe/app:app_defines",
    ],
    includes = ["."],
    visibility = ["//applications/tif2838/units/sysHwCfg:__subpackages__"],
)