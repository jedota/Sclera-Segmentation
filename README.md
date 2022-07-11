## Sclera Segmentation - Usach and hda Proposals

<p class="text-justify"> 
The paper presents a summary of the 2020 Sclera Segmentation Benchmarking Competition (SSBC), the 7th in the series of group benchmarking efforts centred around the problem of sclera segmentation. 
Different from previous editions, the goal of SSBC 2020 was to evaluate the performance of sclera-segmentation models on images captured with mobile devices. 
The competition was used as a platform to assess the sensitivity of existing models to i) differences in mobile devices used for image capture and ii) changes in the ambient acquisition conditions. 
26 research groups registered for SSBC 2020, out of which 13 took part in the final round and submitted a total of 16 segmentation models for scoring. 
These included a wide variety of deep-learning solutions as well as one approach based on standard image processing techniques. Experiments were conducted with three recent datasets. 
Most of the segmentation models achieved relatively consistent performance across images captured with different mobile devices (with slight differences across devices), 
but struggled most with low-quality images captured in challenging ambient conditions, i.e., in an indoor environment and with poor lighting.
</p>

## DenseNet10

The DenseNet is one of the most effcient semanttic segmetator.
The implentation of DenseNet10 is available in: 
https://github.com/Choapinus/DenseNet10

## CGANs2020CL

Formulates the segmentation problem as a patch-to-patch translation task and uses a Conditional Generative Adversarial Network for the segmentation process. A Resnet-101 model is utilised as the backbone of the solution and trained from scratch. Aggressive data augmentation is used during training.
Our generating procedure is heavily based on the implementation of CycleGANs. For more information, please refer to the original implementation:

https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix

Download models: https://www.dropbox.com/s/etnfbowc3j8mh38/ls_gan_r9-v2-tifs.zip?dl=0


![index](https://user-images.githubusercontent.com/45126159/178218059-a8fe86b7-36e0-4a38-b653-d1712c24395b.png)

## Train Options:

|          Options          |      Values             | 
| --------------------------| ------------------------| 
|                batch_size:|   8                     |           
|                     beta1:|  0.5                    |        
|           checkpoints_dir:|  ./checkpoints          |        
|            continue_train:|  False                  |        
|                 crop_size:|  256                    |        
|                  dataroot:|  ./datasets/ocular../	  |  
|              dataset_mode:|  aligned                |        
|                 direction:|  AtoB                   |        
|               display_env:|  main                   |        
|              display_freq:|  400                    |        
|                display_id:|  1                      |        
|             display_ncols:|  4                      |        
|              display_port:|  8097                   |         
|           display_winsize:|  256                    |        
|                     epoch:|  latest                 |        
|               epoch_count:|  1                      |        
|                  gan_mode:|  lsgan                  |       
|                   gpu_ids:|  0                      |        
|                 init_gain:|  0.02                   |        
|                 init_type:|  normal                 |        
|                  input_nc:|  3                      |        
|                   isTrain:|  True                   |        	
|                 lambda_L1:|  100.0                  |        
|                 load_iter:|  0                      |        	
|                 load_size:|  256                    |        
|                        lr:|  0.0002                 |       
|            lr_decay_iters:|  50                     |        
|                 lr_policy:|  linear                 |        
|          max_dataset_size:|  inf                    |        
|                     model:|  pix2pix                |        	
|                  n_epochs:|  200                    |        	
|            n_epochs_decay:|  100                    |        
|                n_layers_D:|  3                      |        
|                      name:|  ls_gan_r9              |        	
|                       ndf:|  64                     |        
|                      netD:|  basic                  |        
|                      netG:|  resnet_9blocks         |        	
|                      ngf: |  64                     |       
|                no_dropout:|  False                  |        
|                   no_flip:|  False                  |        
|                   no_html:|  False                  |        
|                      norm:|  batch                  |        
|               num_threads:|  4                      |        
|                 output_nc:|  3                      |        
|                     phase:|  train                  |        
|                 pool_size:|  0                      |        
|                preprocess:|  resize_and_crop        |        
|                print_freq:|  100                    |        
|              save_by_iter:|  False                  |        
|           save_epoch_freq:|  5                      |        
|          save_latest_freq:|  5000                   |        
|            serial_batches:|  | False                |                                    
|          update_html_freq:| 1000                    |       


## Mask2020CL 

Available soon

## Citation: 

```
@INPROCEEDINGS{9304881,
  author={Vitek, M. and Das, A. and Pourcenoux, Y. and Missler, A. and Paumier, C. and Das, S. and De Ghosh, I. and Lucio, D. R. and Zanlorensi, L. A. and Menotti, D. and Boutros, F. and Damer, N. and Grebe, J. H. and Kuijper, A. and Hu, J. and He, Y. and Wang, C. and Liu, H. and Wang, Y. and Sun, Z. and Osorio-Roig, D. and Rathgeb, C. and Busch, C. and Tapia, J. and Valenzuela, A. and Zampoukis, G. and Tsochatzidis, L. and Pratikakis, I. and Nathan, S. and Suganya, R. and Mehta, V. and Dhall, A. and Raja, K. and Gupta, G. and Khiarak, J. N. and Akbari-Shahper, M. and Jaryani, F. and Asgari-Chenaghlu, M. and Vyas, R. and Dakshit, S. and Peer, P. and Pal, U. and Štruc, V.},
  booktitle={2020 IEEE International Joint Conference on Biometrics (IJCB)}, 
  title={SSBC 2020: Sclera Segmentation Benchmarking Competition in the Mobile Environment}, 
  year={2020},
  volume={},
  number={},
  pages={1-10},
  doi={10.1109/IJCB48548.2020.9304881}}
```

## Questions:
juan.tapia-farias@h-da.de

andres.valenzuela@tocbiometrics.com



