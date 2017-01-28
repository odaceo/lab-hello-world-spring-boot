# -*- mode: ruby -*-
# vi: set ft=ruby :

# Copyright (C) 2015 Odaceo. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/xenial64"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine.
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 9090, host: 9090

  config.vm.provision "shell", privileged: false, 
    path: "https://github.com/odaceo/script-ubuntu-java/raw/master/install.sh"

  config.vm.provision "shell", inline: <<-SHELL
    # Install Git Flow extension
    sudo apt-get install -y git-flow
  SHELL
end
