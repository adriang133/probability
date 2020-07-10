# Copyright 2020 The TensorFlow Probability Authors.
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
# ============================================================================
# [internal] load pytype.bzl (pytype_strict_library)
# [internal] load strict.bzl

package(default_visibility = ["//visibility:public"])

licenses(["notice"])

# pytype_strict
py_library(
    name = "distributions",
    srcs = ["__init__.py"],
    srcs_version = "PY3",
    deps = [
        ":distribution_extensions",
        # [tfp_jax dependency],
    ],
)

# pytype_strict
py_library(
    name = "distribution_extensions",
    srcs = ["distribution_extensions.py"],
    srcs_version = "PY3",
    deps = [
        # jax dep,
        # six dep,
        # [tfp_jax dependency],
        "//oryx/core",
        "//oryx/core/interpreters:inverse",
        "//oryx/core/ppl",
    ],
)

# py_strict
py_test(
    name = "distribution_extensions_test",
    srcs = ["distribution_extensions_test.py"],
    python_version = "PY3",
    deps = [
        ":distributions",
        # absl/testing:absltest dep,
        # absl/testing:parameterized dep,
        # jax dep,
        # numpy dep,
        "//oryx/core",
        "//oryx/core/ppl",
    ],
)