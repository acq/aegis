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

JACKSON_VERSION = "2.12.5"
JUNIT5_API_VERSION = "5.7.1"
JUNIT5_PLATFORM_VERSION="1.7.1"

maven_install(
    artifacts = [
        "com.google.guava:guava:30.1.1-jre",
        "com.squareup.okhttp3:okhttp:4.9.0",
        "com.squareup.okio:okio:2.10.0",
        "com.squareup.retrofit2:retrofit:2.9.0",
        "com.fasterxml.jackson.core:jackson-core:" + JACKSON_VERSION,
        "com.fasterxml.jackson.core:jackson-annotations:" + JACKSON_VERSION,
        "com.fasterxml.jackson.core:jackson-databind:" + JACKSON_VERSION,
        "org.junit.platform:junit-platform-commons:" + JUNIT5_PLATFORM_VERSION,
        "org.junit.platform:junit-platform-console:" + JUNIT5_PLATFORM_VERSION,
        "org.junit.platform:junit-platform-engine:" + JUNIT5_PLATFORM_VERSION,
        "org.junit.platform:junit-platform-launcher:" + JUNIT5_PLATFORM_VERSION,
        "org.junit.platform:junit-platform-suite-api:" + JUNIT5_PLATFORM_VERSION,
        "org.junit.jupiter:junit-jupiter-api:" + JUNIT5_API_VERSION,
        "org.junit.jupiter:junit-jupiter-engine:" + JUNIT5_API_VERSION,
        "org.junit.jupiter:junit-jupiter-params:" + JUNIT5_API_VERSION,
    ],
    repositories = [
        "https://repo1.maven.org/maven2",
    ],
    fetch_sources = True,
)
