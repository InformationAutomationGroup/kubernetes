load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "state.go",
        "state_file.go",
        "state_mem.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/kubelet/cm/cpumanager/state",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/kubelet/cm/cpuset:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["state_file_test.go"],
    embed = [":go_default_library"],
    importpath = "k8s.io/kubernetes/pkg/kubelet/cm/cpumanager/state",
    deps = ["//pkg/kubelet/cm/cpuset:go_default_library"],
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
    visibility = ["//visibility:public"],
)
