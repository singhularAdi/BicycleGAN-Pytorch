# BicycleGAN-Pytorch

This repositiory is a reimplementation of _Zhu, J., et al. "Toward multimodal image-to-image translation.(2017)." arXiv preprint arXiv:1711.11586 (2017)_. 

To run, set the project_folder variable and root_dir as required. The directory structure should be as follows:

    .
    ├── datasets                    
    │   ├── edge2shoe          # edge2shoe dataset as available on the website
    │   └── ...        
    ├── models
    ├── losses
    └── plots
    
 Post setup, simple run all cells sequentially. The model will train and compute the LPIPS and FID score for the trained model.
 
 Inference can be performed by 
 
 ```
z_real = torch.rand([1,8])
# outline is an outline from the original distribution
fake_images = generator(norm(torch.unsqueeze(outline,0).to(device)),z_real.to(device))
 ```
