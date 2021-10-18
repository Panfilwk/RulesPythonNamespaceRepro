load("@rules_python//python/pip_install:requirements.bzl", "compile_pip_requirements")
load("@requirements_install//:requirements.bzl", requirement_install = "requirement")
load("@requirements_parse//:requirements.bzl", requirement_parse = "requirement")

exports_files(["requirements.in"])

compile_pip_requirements(
    name = "requirements",
    extra_args = ["--allow-unsafe"],
)

py_binary(
    name = "install_test",
    srcs = ["imports.py"],
    main = "imports.py",
    deps = [requirement_install("google-api-core")],
)

py_binary(
    name = "parse_test",
    srcs = ["imports.py"],
    main = "imports.py",
    deps = [requirement_parse("google-api-core")],
)
