<!--
 * @Date: 2021-04-14 14:12:18
 * @Author: Qing Shuai
 * @LastEditors: Qing Shuai
 * @LastEditTime: 2021-04-14 16:11:24
 * @FilePath: /Mirrored-Human-public/doc/evaluation.md
-->
# Evaluation

## Data Preparation

Download our data [zju-m-seq1](https://www.dropbox.com/s/fjyhgbcbe8cpoa5/zju-m-seq1.zip?dl=0) and extract it.

Set the `data` and `out`:
```bash
data=<path_to_evaluation_dataset>
out=<path_to_output>
```

## Run
```bash
python3 apps/demo/1v1p_mirror.py ${data} --out ${out} --vis_smpl --verbose --gtK --normal --step 100 --body body15
```

## Report

```bash
python3 scripts/postprocess/eval_k3d.py ${data}/keypoints3d --cam ${data}/ --out ${out}/keypoints3d --mono --step_gt 100 --type_e body15
```
