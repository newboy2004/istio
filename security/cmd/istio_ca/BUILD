load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "main.go",
        "markdown.go",
    ],
    visibility = ["//visibility:private"],
    deps = [
        "//security/cmd/istio_ca/version:go_default_library",
        "//security/pkg/cmd:go_default_library",
        "//security/pkg/pki/ca:go_default_library",
        "//security/pkg/pki/ca/controller:go_default_library",
        "//security/pkg/server/grpc:go_default_library",
        "@com_github_golang_glog//:go_default_library",
        "@com_github_spf13_cobra//:go_default_library",
        "@com_github_spf13_cobra//doc:go_default_library",
        "@io_k8s_client_go//kubernetes:go_default_library",
        "@io_k8s_client_go//kubernetes/typed/core/v1:go_default_library",
        "@io_k8s_client_go//rest:go_default_library",
        "@io_k8s_client_go//tools/clientcmd:go_default_library",
    ],
)

go_binary(
    name = "istio_ca",
    library = ":go_default_library",
    linkstamp = "istio.io/istio/security/cmd/istio_ca/version",
    visibility = ["//visibility:public"],
)
