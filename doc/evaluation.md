# Evaluation

## Data Preparation

## Run
```bash
python3 easymocap/demo_1v1pmf_smpl_mirror.py ${data} --out ${out} --body body15 --step 100 --gtK
```

## Report

```bash
python3 scripts/postprocess/eval_k3d.py ${data}/output/keypoints3d --cam ${data}/ --out ${out}/keypoints3d --mono --step_gt 100 --type_e body15
```
