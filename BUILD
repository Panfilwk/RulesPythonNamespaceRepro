load("@rules_python//python/pip_install:requirements.bzl", "compile_pip_requirements")

exports_files(["requirements.in"])

compile_pip_requirements(
    name = "requirements",
    extra_args = ["--allow-unsafe"],
)
