# final_nerf
原版nerf实现\
数据使用自己拍摄的水杯图片77张在my_object/images下，由colmap进行稀疏重建估计相机参数后，在LLFF中转换为llff数据集，测试集每8张留出1张。\
在LLFF项目目录终端下运行imgs2poses.py最后得到用于训练的llff格式数据\
下载nerf-pytorch仓库https://github.com/yenchenlin/nerf-pytorch并安装依赖\
将my_object放入nerf-pytorch/data/nerf_llff_data中,my_object.text放入nerf-pytorch/configs\
用run_nerf.py替换原run_nerf.py\
在nerf-pytorch目录终端下运行python run_nerf.py --config configs/my_object.txt进行训练\
运行python run_nerf.py --config configs/my_object.txt --render_only进行渲染\
tensorboard --logdir=logs/my_object启用tensorboard



