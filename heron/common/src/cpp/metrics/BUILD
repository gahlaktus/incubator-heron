package(default_visibility = ["//visibility:public"])

cc_library(
    name = "metrics-cxx",
    srcs = [
        "assignable-metric.cpp",
        "count-metric.cpp",
        "mean-metric.cpp",
        "metrics-mgr-st.cpp",
        "metricsmgr-client.cpp",
        "multi-assignable-metric.cpp",
        "multi-count-metric.cpp",
        "multi-mean-metric.cpp",
        "time-spent-metric.cpp",
        "tmaster-metrics.cpp",

        "assignable-metric.h",
        "count-metric.h",
        "imetric.h",
        "mean-metric.h",
        "metrics-mgr-st.h",
        "metrics.h",
        "metricsmgr-client.h",
        "multi-assignable-metric.h",
        "multi-count-metric.h",
        "multi-mean-metric.h",
        "time-spent-metric.h",
        "tmaster-metrics.h",
    ],
    copts = [
        "-Iheron",
        "-Iheron/common/src/cpp",
        "-I$(GENDIR)/heron",
        "-I$(GENDIR)/heron/common/src/cpp",
    ],
    deps = [
        "//config:config-cxx",
        "//heron/proto:proto-cxx",
        "//heron/common/src/cpp/network:network-cxx",
        "//heron/common/src/cpp/config:config-cxx",
        "@com_github_google_glog//:glog",
        "@com_google_protobuf//:protobuf",
    ] + select({
        "//tools/platform:darwin": [],
        "//conditions:default": ["@org_nongnu_libunwind//:libunwind"],
    }),
    linkstatic = 1,
)
