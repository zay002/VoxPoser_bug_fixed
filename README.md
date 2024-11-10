# 目前解决的问题是在reset()函数调用引起的渲染出错（内核崩溃）。
# 问题原因在rlbench_env.py中，点云的数据类型出错，查询Open3D文档发现，points和colors都应为np.float64类型，而原代码中实为unit8，已修改

## 上述问题解决，环境成功reset和visualize以后，在voxposer_ui(instruction)运行时再次出现问题
## 初步认为prompt生成存在问题，在我的机器上仅有部分instruction能够不报错生成prompt
## 即使生成prompt并由GPT返回结果后，在generate code后也会产生报错，我正在寻找原因

### 系统环境为Ubuntu 20.04虚拟机，所有模块和前置已正确安装