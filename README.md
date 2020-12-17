# cuda_installation
- 看显卡设备是否存在， 下面查询NVIDIA显卡
  > lspci | grep -i nvidia

- 查看驱动是否已经运行
  > lsmod | grep nvidia

- 删除nvidia 驱动命令(更新驱动才需要)
  > sudo apt-get remove --purge nvidia*

- 删除cuda
  > sudo apt-get autoremove cuda

- 重启(可选)
  > sudo reboot

- 安装cuda
  > sudo dpkg -i cuda-repo-ubuntu1704-9-0-local_9.0.176-1_amd64.deb

  > sudo apt-key add /var/cuda-repo-`<version>`/7fa2af80.pub
  
  > sudo apt-get update

  > sudo apt-get install cuda

- 同时安装多个版本
  > sudo sh cuda_`<version>`.run
  （安装过程中，nvidia driver选择no，创建软链接选择no）

  > sudo rm -rf /usr/local/cuda

  > sudo ln -s /usr/local/cuda-10.1 /usr/local/cuda

  > nvcc --version (检查当前cuda版本)
