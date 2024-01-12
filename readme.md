### windows对战：
* 修改dppo\envs\etc.py的MOZIPATH 为本机墨子推演系统的bin目录文件夹，其他推演速度，决策步长也可以设置。
* 设置完成后，启动main_versus.py：就可以运行该案例，启动对战。

### windows训练：
* 启动cmd命令行，切换到 mozi_ai_sdk/dppo文件夹，启动learner训练： 
  python -m train_ppo --job_name learner --log_num 8 --save_dir ./bin/checkpoints/6
* 启动另一个命令行，切换到 mozi_ai_sdk/dppo文件夹，启动actor， 进⾏采样学习：python -m train_ppo --job_name actor localhost --log_num 6 --save_dir ./bin/checkpoints/3
  python -m train_ppo --job_name actor --log_num 8 --save_dir ./bin/checkpoints/6
* D:\project\mozi\moziai\mozi_ai_sdk\dppo\envs\etc.py修改环境想定及训练参数