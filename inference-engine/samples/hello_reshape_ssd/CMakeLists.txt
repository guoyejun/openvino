# Copyright (C) 2018-2020 Intel Corporation

# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at

#      http://www.apache.org/licenses/LICENSE-2.0

# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

ie_add_sample(NAME hello_reshape_ssd
              SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/main.cpp"
              HEADERS "${CMAKE_CURRENT_SOURCE_DIR}/reshape_ssd_extension.hpp"
              OPENCV_DEPENDENCIES imgcodecs)

find_package(ngraph REQUIRED)
target_link_libraries(hello_reshape_ssd PRIVATE ${NGRAPH_LIBRARIES})
