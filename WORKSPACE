load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive", "http_file")

# ===== Abseil =====

http_archive(
    name = "com_google_absl",
    sha256 = "38f5113dff685ddfd3bf53d1473a18dfcfe8de89ee7c9b3708e3a070274c6b38",
    strip_prefix = "abseil-cpp-e63a5a61045e516b7b3dbca090e2b9ff1d057e46",
    urls = [
        "https://mirror.bazel.build/github.com/abseil/abseil-cpp/archive/e63a5a61045e516b7b3dbca090e2b9ff1d057e46.tar.gz",
        "https://github.com/abseil/abseil-cpp/archive/e63a5a61045e516b7b3dbca090e2b9ff1d057e46.tar.gz",
    ],
)

# CCTZ (Time-zone framework).
http_archive(
    name = "com_googlesource_code_cctz",
    strip_prefix = "cctz-master",
    urls = ["https://github.com/google/cctz/archive/master.zip"],
)

# ===== re2 =====

http_archive(
    name = "com_googlesource_code_re2",
    sha256 = "5306526bcdf35ff34c67913bef8f7b15a3960f4f0ab3a2b6a260af4f766902d4",
    strip_prefix = "re2-c4f65071cc07eb34d264b25f7b9bbb679c4d5a5a",
    urls = [
        "https://mirror.bazel.build/github.com/google/re2/archive/c4f65071cc07eb34d264b25f7b9bbb679c4d5a5a.tar.gz",
        "https://github.com/google/re2/archive/c4f65071cc07eb34d264b25f7b9bbb679c4d5a5a.tar.gz",
    ],
)

# ===== protobuf =====
# See https://bazel.build/blog/2017/02/27/protocol-buffers.html

http_archive(
    name = "com_google_protobuf",
    sha256 = "2ddbc2f0c30e8f9ee7cc8281707859827c143a1dc088f74d38aca66fe6b664a2",
    strip_prefix = "protobuf-93a18cf2be6d590d23f34757a32133306e290ca9",
    urls = [
        "https://mirror.bazel.build/github.com/google/protobuf/archive/93a18cf2be6d590d23f34757a32133306e290ca9.tar.gz",
        "https://github.com/google/protobuf/archive/93a18cf2be6d590d23f34757a32133306e290ca9.tar.gz",
    ],
)

load("@com_google_protobuf//:protobuf_deps.bzl", "protobuf_deps")
protobuf_deps()

http_archive(
    name = "com_google_protobuf_cc",
    sha256 = "2ddbc2f0c30e8f9ee7cc8281707859827c143a1dc088f74d38aca66fe6b664a2",
    strip_prefix = "protobuf-93a18cf2be6d590d23f34757a32133306e290ca9",
    urls = [
        "https://mirror.bazel.build/github.com/google/protobuf/archive/93a18cf2be6d590d23f34757a32133306e290ca9.tar.gz",
        "https://github.com/google/protobuf/archive/93a18cf2be6d590d23f34757a32133306e290ca9.tar.gz",
    ],
)

# Required by protobuf.
http_archive(
    name = "bazel_skylib",
    sha256 = "bbccf674aa441c266df9894182d80de104cabd19be98be002f6d478aaa31574d",
    strip_prefix = "bazel-skylib-2169ae1c374aab4a09aa90e65efe1a3aad4e279b",
    urls = ["https://github.com/bazelbuild/bazel-skylib/archive/2169ae1c374aab4a09aa90e65efe1a3aad4e279b.tar.gz"],
)

# ===== googletest =====

http_archive(
    name = "com_google_googletest",
    sha256 = "c08d14e829bf5e2ab3bda2cc80a061126f2a430fcecdb9e9c0fc8023fd39d9a5",
    strip_prefix = "googletest-07f4869221012b16b7f9ee685d94856e1fc9f361",
    urls = [
        "https://mirror.bazel.build/github.com/google/googletest/archive/07f4869221012b16b7f9ee685d94856e1fc9f361.tar.gz",
        "https://github.com/google/googletest/archive/07f4869221012b16b7f9ee685d94856e1fc9f361.tar.gz",
    ],
)

# ===== benchmark =====

http_archive(
    name = "com_google_benchmark",
    build_file = "@//:benchmark.BUILD",
    sha256 = "e7334dd254434c6668e33a54c8f839194c7c61840d52f4b6258eee28e9f3b20e",
    strip_prefix = "benchmark-1.1.0",
    urls = [
        "https://mirror.bazel.build/github.com/google/benchmark/archive/v1.1.0.tar.gz",
        "https://github.com/google/benchmark/archive/v1.1.0.tar.gz",
    ],
)

# ===== utf =====

http_archive(
    name = "utf_archive",
    build_file = "@//:utf.BUILD",
    sha256 = "262a902f622dcd28e05b8a4be10da0aa3899050d0be8f4a71780eed6b2ea65ca",
    urls = [
        "https://mirror.bazel.build/9fans.github.io/plan9port/unix/libutf.tgz",
        "https://9fans.github.io/plan9port/unix/libutf.tgz",
    ],
)

# ===== gflags =====

http_archive(
    name = "com_github_gflags_gflags",
    sha256 = "466c36c6508a451734e4f4d76825cf9cd9b8716d2b70ef36479ae40f08271f88",
    strip_prefix = "gflags-2.2.0",
    urls = [
        "https://mirror.bazel.build/github.com/gflags/gflags/archive/v2.2.0.tar.gz",
        "https://github.com/gflags/gflags/archive/v2.2.0.tar.gz",
    ],
)

# ===== glog =====

http_archive(
    name = "com_github_glog_glog",
    build_file = "@//:glog.BUILD",
    sha256 = "7580e408a2c0b5a89ca214739978ce6ff480b5e7d8d7698a2aa92fadc484d1e0",
    strip_prefix = "glog-0.3.5",
    urls = [
        "https://mirror.bazel.build/github.com/google/glog/archive/v0.3.5.tar.gz",
        "https://github.com/google/glog/archive/v0.3.5.tar.gz",
    ],
)

# ===== xpdf =====

http_archive(
    name = "xpdf_archive",  # GPLv2
    build_file = "@//:xpdf.BUILD",
    sha256 = "11390c74733abcb262aaca4db68710f13ffffd42bfe2a0861a5dfc912b2977e5",
    urls = [
        "https://mirror.bazel.build/download.openpkg.org/components/cache/xpdf/xpdf-3.04.tar.gz",
        "http://download.openpkg.org/components/cache/xpdf/xpdf-3.04.tar.gz",
    ],
)

# ===== libpfm4 =====

http_archive(
    name = "libpfm4_git",
    build_file = "@//:libpfm4.BUILD",
    sha256 = "9193787a73201b4254e3669243fd71d15a9550486920861912090a09f366cf68",
    strip_prefix = "libpfm-4.8.0",
    urls = ["https://iweb.dl.sourceforge.net/project/perfmon2/libpfm4/libpfm-4.8.0.tar.gz"],
)

# ===== tinyxml2 =====

http_archive(
    name = "tinyxml2_git",  # zlib license
    build_file = "@//:tinyxml2.BUILD",
    sha256 = "cdf0c2179ae7a7931dba52463741cf59024198bbf9673bf08415bcb46344110f",
    strip_prefix = "tinyxml2-6.2.0",
    urls = [
        "https://mirror.bazel.build/github.com/leethomason/tinyxml2/archive/6.2.0.tar.gz",
        "https://github.com/leethomason/tinyxml2/archive/6.2.0.tar.gz",
    ],
)

# ===== or-tools =====

http_archive(
    name = "or_tools_git",  # Apache 2.0
    sha256 = "d02fb68e1967fc3b8fed622755187a3df9cc175fe816cd149278d26b51519529",
    strip_prefix = "or-tools-53189020e3f995715a935aab7355357ce658fb76",
    urls = [
        "https://mirror.bazel.build/github.com/google/or-tools/archive/53189020e3f995715a935aab7355357ce658fb76.tar.gz",
        "https://github.com/google/or-tools/archive/53189020e3f995715a935aab7355357ce658fb76.tar.gz",
    ],
)

# ===== LLVM =====

http_archive(
    name = "llvm_git",
    build_file = "@//:llvm.BUILD",
    sha256 = "95b3a609cc0db719ea19daed2689a770f97aea974a3d2cf70468d3b067e8b068",
    strip_prefix = "llvm-project-c10248829357fd90030ba091e01b6c253e5848f1/llvm",
    urls = [
        # Please don't refactor out the SHA; if URLs aren't greppable,
        # we can't offer you an asynchronous mirroring service that
        # allows this huge archive to download in one second.
        "https://mirror.bazel.build/github.com/llvm/llvm-project/archive/c10248829357fd90030ba091e01b6c253e5848f1.tar.gz",
        "https://github.com/llvm/llvm-project/archive/c10248829357fd90030ba091e01b6c253e5848f1.tar.gz",
    ],
)

# ===== Intel SDM =====

http_file(
    name = "intel_sdm_pdf",
    sha256 = "662feb7d46310ea723f431c35d6b495fda3960cfacd4eb3136d1a30cb8a9ed37",
    urls = ["https://software.intel.com/content/dam/develop/external/us/en/documents-tps/325462-sdm-vol-1-2abcd-3abcd.pdf"],
)

# ==============================================================================
# Transitive Dependencies:
# See https://bazel.build/versions/master/docs/external.html#transitive-dependencies
# ==============================================================================

http_archive(
    name = "glpk",  # GPLv3
    build_file = "@or_tools_git//bazel:glpk.BUILD",
    sha256 = "9a5dab356268b4f177c33e00ddf8164496dc2434e83bd1114147024df983a3bb",
    urls = [
        "https://mirror.bazel.build/ftp.gnu.org/gnu/glpk/glpk-4.52.tar.gz",
        "https://ftp.gnu.org/gnu/glpk/glpk-4.52.tar.gz",
    ],
)
