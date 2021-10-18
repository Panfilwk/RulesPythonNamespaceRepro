load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_python",
    sha256 = "934c9ceb552e84577b0faf1e5a2f0450314985b4d8712b2b70717dc679fdc01b",
    url = "https://github.com/bazelbuild/rules_python/releases/download/0.3.0/rules_python-0.3.0.tar.gz",
)

load("@rules_python//python:pip.bzl", "pip_install", "pip_parse")

pip_install(
    name = "requirements_install",
    requirements = "//:requirements.txt"
)

pip_parse(
    name = "requirements_parse",
    requirements_lock = "//:requirements.txt"
)
