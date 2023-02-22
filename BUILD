# A database of instructions and a parser for the Intel(r) 64 and IA-32
# Architectures Software Developer's Manual.

package(default_visibility = ["//visibility:public"])

licenses(["notice"])

exports_files([
    "LICENSE",
    "llvm.bzl",
])

# Generates a text file with the version of LLVM used in the build. The version
# is required to generate some of the LLVM headers, but it is not possible to
# get the version from inside the @llvm_git repository.
# We use the git hash or tag as a version string; this hash or tag is extracted
# from the llvm_git rule in the WORKSPACE file, to avoid duplication of this
# information.
genrule(
    name = "llvm_git_revision_gen",
    srcs = ["WORKSPACE"],
    outs = ["llvm_git_revision"],
    cmd = r"""perl -ne 'if (/strip_prefix = "llvm-project-(.*)\/llvm"/) { print "$$1\n"; exit } ' < $< > $@""",
    visibility = ["//visibility:public"],
)

package_group(
    name = "internal_users",
    packages = [
        "//exegesis/...",
        "//llvm_sim/...",
    ],
)

load("@hedron_compile_commands//:refresh_compile_commands.bzl", "refresh_compile_commands")
refresh_compile_commands(
    name = "refresh_compile_commands",
    targets = {
      # "//exegesis/...": "--copt='-DNO_THREADS'",
      # "//exegesis/x86/...": "--copt='-DNO_THREADS'",
      "//exegesis/base/...": "--copt='-DNO_THREADS'",
      "//exegesis/tools/...": "--copt='-DNO_THREADS'",
      "//exegesis/proto/...": "--copt='-DNO_THREADS'",
      # "//exegesis/tools:parse_intel_sdm": "--copt='-DNO_THREADS' --copt=-I.",
      # "//exegesis/tools:parse_arm_xml": "--copt='-DNO_THREADS' --copt=-I.",
      # "//exegesis/tools:pdf2proto": "--copt='-DNO_THREADS' --copt=-I.",
      # "//exegesis/tools:proto_patch_helper": "--copt='-DNO_THREADS' --copt=-I.",
      # "//exegesis/tools:proto_patch_migrate": "--copt='-DNO_THREADS' --copt=-I.",
    },
)
