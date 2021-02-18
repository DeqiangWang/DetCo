# DetCo: Unsupervised Contrastive Learning for Object Detection
[arxiv link](https://arxiv.org/abs/2102.04803)

## Highlights

- State-of-the-art transfer performance on dense prediction tasks.
- Improving  1.6/1.2/1.0 AP than supervised ImageNet pretrain on Mask RCNN-C4/FPN/RetinaNet with COCO 1x schedule.
- Comprehensively improving most instance-level detection and semantic segmentation tasks.

## Pipeline
![image-20190807160835333](imgs/pipeline.png)


## Performances
![Graph](imgs/res_coco.png)

-----

![Graph](imgs/res2_coco.png)

----

![Graph](imgs/other_res2.png)

-----

![Graph](imgs/vis.png)

-----

![Graph](imgs/vis2.png)



## Codes

### Pretext Task Pretrain

### Transfer to Downstream tasks

We provide training scripts on COCO, because the performacen of COCO is more stable than VOC and Cityscapes.

We provide Mask RCNN-C4, Mask RCNN-FPN and RetinaNet with 12k, 90k and 180k iterations.

```
sh tools_local/dist_test_coco.sh $PTH $WORK_DIR
```

For example:
```
sh tools_local/dist_test_coco.sh benchmarks/detection/pths/detco_200ep_AA.pkl benchmarks/detection/work_dirs/detco_AA
```

## Download Models
[DetCO-200ep]  [DetCO-200ep-AA]

Coming Soon

## Citations
Please consider citing our paper in your publications if the project helps your research. BibTeX reference is as follows.

```
@misc{xie2021detco,
      title={DetCo: Unsupervised Contrastive Learning for Object Detection}, 
      author={Enze Xie and Jian Ding and Wenhai Wang and Xiaohang Zhan and Hang Xu and Zhenguo Li and Ping Luo},
      year={2021},
      eprint={2102.04803},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```



## Acknowledges
We would like to thank Huawei AI Theory Group to support 200+ V100 GPUs for this research project without which this work would not be possible.

## License

For academic use, this project is licensed under the 2-clause BSD License - see the LICENSE file for details. For commercial use, please contact the authors. 