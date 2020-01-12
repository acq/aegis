load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_JVM_EXTERNAL_TAG = "2.5"
RULES_JVM_EXTERNAL_SHA = "249e8129914be6d987ca57754516be35a14ea866c616041ff0cd32ea94d2f3a1"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
        "junit:junit:4.12",
        "com.google.guava:guava:28.0-jre",
        "com.squareup.okhttp3:okhttp:4.2.1",
        "com.squareup.okio:okio:2.4.3",
        "com.squareup.retrofit2:retrofit:2.7.0",
        "com.fasterxml.jackson.core:jackson-core:2.10.0",
        "com.fasterxml.jackson.core:jackson-annotations:2.10.0",
        "com.fasterxml.jackson.core:jackson-databind:2.10.0",
    ],
    repositories = [
        "http://uk.maven.org/maven2",
        "https://jcenter.bintray.com/",
    ],
    fetch_sources = True,
)
