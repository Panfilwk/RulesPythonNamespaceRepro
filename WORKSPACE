load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_python",
    sha256 = "954aa89b491be4a083304a2cb838019c8b8c3720a7abb9c4cb81ac7a24230cea",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/rules_python/releases/download/0.4.0/rules_python-0.4.0.tar.gz",
        "https://github.com/bazelbuild/rules_python/releases/download/0.4.0/rules_python-0.4.0.tar.gz",
    ],
)

load("@rules_python//python:pip.bzl", "pip_install", "pip_parse")

pip_install(
    name = "requirements_install",
    requirements = "//:requirements.txt",
)

pip_parse(
    name = "requirements_parse",
    requirements_lock = "//:requirements.txt",
)

load("@requirements_parse//:requirements.bzl", "install_deps")

install_deps()
