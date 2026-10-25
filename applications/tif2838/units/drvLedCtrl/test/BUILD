cc_test(
    name = "drvLedCtrl_test",
    size = "small",
    srcs = [
        "drvLedCtrl_test.cc",
        "//applications/tif2838/units/drvLedCtrl/code:srcs",
        "//applications/tif2838/units/drvLedCtrl/code:hdrs",
    ],
    deps = [
        "@googletest//:gtest",
        "@googletest//:gtest_main",
        "@emb_platform//c2000/mcal/f28p65/test:mcal_f28p65x_h",
    ],
    includes = [
        "../code"
    ],
)
