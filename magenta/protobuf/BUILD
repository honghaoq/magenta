# Copyright 2016 Google Inc. All Rights Reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# Description:
# Magenta protocol buffers.

package(
    default_visibility = ["//magenta:__subpackages__"],
    features = ["-layering_check"],
)

load("@protobuf//:protobuf.bzl", "cc_proto_library")
load("@protobuf//:protobuf.bzl", "py_proto_library")

py_proto_library(
    name = "music_py_pb2",
    srcs = ["music.proto"],
    srcs_version = "PY2AND3",
    protoc = "@protobuf//:protoc",
    default_runtime = "@protobuf//:protobuf_python",
)

cc_proto_library(
   name = "music_proto",
   srcs = ["music.proto"],
   protoc = "@protobuf//:protoc",
   default_runtime = "@protobuf//:protobuf",
)

py_proto_library(
    name = "generator_py_pb2",
    srcs = ["generator.proto"],
    deps = [":music_py_pb2"],
    srcs_version = "PY2AND3",
    protoc = "@protobuf//:protoc",
    default_runtime = "@protobuf//:protobuf_python",
)

cc_proto_library(
   name = "generator_proto",
   srcs = ["generator.proto"],
   deps = [":music_proto"],
   protoc = "@protobuf//:protoc",
   default_runtime = "@protobuf//:protobuf",
)