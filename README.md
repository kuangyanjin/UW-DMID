# UW-DMID
underwater single photon image used DMID

# 先这个
python main_for_real_NT.py \
  --clean_path ./data/CC/GT/ \
  --noisy_path ./data/CC/Noisy/ \
  --datatype CC



# 确保路径正确
python main_for_real.py \
  --input_dir ./results/nn_CC/ \
  --output_dir ./final_results/ \
  --datatype CC \
  --eval_time 3 \
  --S_t 1  \
  --R_t 3  \
  --eta 0.85

在使用python main_for_real.py时，确保noisy_path,指向的是python main_for_real_NT.py中生成的pt文件
eg: './results/nn_FMDD/FMDD.pt'

clean_path'指向NT时同样用的clean path图像文件夹
eg: './data/FMDD/GT/'