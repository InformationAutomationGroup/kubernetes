load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "diff.go",
        "formatter.go",
        "pretty.go",
        "zero.go",
    ],
    importpath = "github.com/kr/pretty",
    visibility = ["//visibility:public"],
    deps = ["//vendor/github.com/kr/text:go_default_library"],
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
