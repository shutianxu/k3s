package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "defaults.go",
        "register_predicates.go",
        "register_priorities.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/scheduler/algorithmprovider/defaults",
    deps = [
        "//pkg/features:go_default_library",
        "//pkg/scheduler:go_default_library",
        "//pkg/scheduler/algorithm:go_default_library",
        "//pkg/scheduler/algorithm/predicates:go_default_library",
        "//pkg/scheduler/algorithm/priorities:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/util/feature:go_default_library",
        "//vendor/k8s.io/klog:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["defaults_test.go"],
    embed = [":go_default_library"],
    deps = [
        "//pkg/scheduler/algorithm/predicates:go_default_library",
        "//pkg/scheduler/algorithm/priorities:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/sets:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
