load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_library",
    "envoy_package",
)

licenses(["notice"])  # Apache 2

envoy_package()

envoy_cc_library(
    name = "overload_manager_interface",
    hdrs = ["overload_manager.h"],
    deps = [
        ":thread_local_overload_state",
        "//include/envoy/event:dispatcher_interface",
        "//include/envoy/thread_local:thread_local_interface",
        "//source/common/singleton:const_singleton",
    ],
)

envoy_cc_library(
    name = "thread_local_overload_state",
    hdrs = ["thread_local_overload_state.h"],
    deps = [
        "//include/envoy/event:scaled_timer_minimum",
        "//include/envoy/event:timer_interface",
        "//include/envoy/thread_local:thread_local_object",
        "//source/common/common:interval_value",
    ],
)
