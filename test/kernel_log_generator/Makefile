# Copyright 2017 The Kubernetes Authors.
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

# Build the kernel problem generator.

.PHONY: all build push

PROJ ?= staging-k8s.gcr.io
TAG := 0.1

all: push

build:
	docker build -t $(PROJ)/kernel_log_generator:$(TAG) .

push:
	gcloud docker -- push $(PROJ)/kernel_log_generator:$(TAG)

clean:
	docker rmi $(PROJ)/kernel_log_generator:$(TAG)
