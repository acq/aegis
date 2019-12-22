java_library(
    name = "net_library",
    srcs = glob(["*.java"]),
    deps = [
        "@maven//:junit_junit",
        "@maven//:com_google_guava_guava",
        "@maven//:com_squareup_okhttp3_okhttp",
        "@maven//:com_squareup_okio_okio",
        "@maven//:com_squareup_retrofit2_retrofit",

    ],
)

java_binary(
    name = "net",
    runtime_deps = [":net_library"],
    main_class = "net.Test"
)
