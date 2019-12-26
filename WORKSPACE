workspace(name = "com_google_jsinterop_base")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:jvm.bzl", "jvm_maven_import_external")

# Load j2cl repository

http_archive(
    name = "com_google_j2cl",
    strip_prefix = "j2cl-master",
    url = "https://github.com/google/j2cl/archive/master.zip",
)

load("@com_google_j2cl//build_defs:repository.bzl", "load_j2cl_repo_deps")

load_j2cl_repo_deps()

load("@com_google_j2cl//build_defs:rules.bzl", "setup_j2cl_workspace")

setup_j2cl_workspace()

jvm_maven_import_external(
    name = "org_gwtproject_gwt_dev",
    artifact = "com.google.gwt:gwt-dev:2.8.1",
    server_urls = ["https://repo1.maven.org/maven2/"],
    licenses = ["notice"],
)
