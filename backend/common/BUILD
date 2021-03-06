#
# Copyright 2020 Google LLC
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

package(default_visibility = ["//:__subpackages__"])

licenses(["unencumbered"])

cc_library(
    name = "ids",
    hdrs = [
        "ids.h",
    ],
    deps = [
        "@com_google_absl//absl/base:core_headers",
        "@com_google_absl//absl/strings",
        "@com_google_absl//absl/synchronization",
    ],
)

cc_test(
    name = "ids_test",
    srcs = [
        "ids_test.cc",
    ],
    deps = [
        ":ids",
        "//tests/common:proto_matchers",
        "@com_github_grpc_grpc//:grpc++",
        "@com_google_absl//absl/synchronization",
        "@com_google_googletest//:gtest_main",
        "@com_google_zetasql//zetasql/base/testing:status_matchers",
    ],
)

cc_library(
    name = "indexing",
    srcs = [
        "indexing.cc",
    ],
    hdrs = [
        "indexing.h",
    ],
    deps = [
        ":rows",
        "//backend/datamodel:key",
        "//backend/datamodel:value",
        "//backend/schema/catalog:schema",
        "@com_google_zetasql//zetasql/public:value",
    ],
)

cc_test(
    name = "indexing_test",
    srcs = [
        "indexing_test.cc",
    ],
    deps = [
        "indexing",
        "//tests/common:proto_matchers",
        "@com_github_grpc_grpc//:grpc++",
        "@com_google_googletest//:gtest_main",
        "@com_google_zetasql//zetasql/base/testing:status_matchers",
    ],
)

cc_library(
    name = "case",
    hdrs = [
        "case.h",
    ],
    deps = [
        "@com_google_absl//absl/container:flat_hash_map",
        "@com_google_absl//absl/container:flat_hash_set",
        "@com_google_absl//absl/strings",
        "@com_google_zetasql//zetasql/base:case",
    ],
)

cc_test(
    name = "case_test",
    srcs = [
        "case_test.cc",
    ],
    deps = [
        ":case",
        "//tests/common:proto_matchers",
        "@com_github_grpc_grpc//:grpc++",
        "@com_google_absl//absl/container:flat_hash_set",
        "@com_google_googletest//:gtest_main",
        "@com_google_zetasql//zetasql/base/testing:status_matchers",
    ],
)

cc_library(
    name = "rows",
    srcs = [
        "rows.cc",
    ],
    hdrs = [
        "rows.h",
    ],
    deps = [
        "//backend/datamodel:value",
        "//backend/schema/catalog:schema",
        "//common:errors",
    ],
)

cc_test(
    name = "rows_test",
    srcs = [
        "rows_test.cc",
    ],
    deps = [
        "rows",
        "//tests/common:proto_matchers",
        "@com_github_grpc_grpc//:grpc++",
        "@com_google_googletest//:gtest_main",
        "@com_google_zetasql//zetasql/base/testing:status_matchers",
    ],
)

cc_library(
    name = "variant",
    hdrs = [
        "variant.h",
    ],
)
