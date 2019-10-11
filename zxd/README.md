# Install
## 环境
- python 3.6
- ubuntu 18
- cuda 9
- torch 0.4.0
## Error
1) bash install_scripts.sh

error1:

权限不够 

办法： 在install_scripts.sh中改成chmod +x ./make.sh

error2: 

rm: cannot remove 'Resample2d_kernel.o': No such file or directory

rm: cannot remove '../_ext': No such file or directory 

办法： 重新运行一遍

2) 下载demo and model weights老失败 

办法：多试几次就会成功

3) python tools/video_inpaint.py 

ModuleNotFoundError: No module named 'models.FlowNet2_Models.resample2d_package._ext' 

原因： bash install_scripts.sh没有成功 

办法： 在pycharm终端下 （桌面终端应该也行，没试） 
```bash
cd models/FlowNet2_Models/resample2d_package/
./make.sh （若出现cannot remove，再执行一遍）
```

