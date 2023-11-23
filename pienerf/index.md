---
layout: project_page
permalink: /pienerf/

title: "PIE-NeRF🍕: Physics-based Interactive Elastodynamics with NeRF"
authors:
    <a href="https://fytalon.github.io/">Yutao Feng</a><sup>1,2</sup>, <a href="https://shayito.github.io/">Yintong Shang</a><sup>1</sup>, <a href="https://xuan-li.github.io/">Xuan Li</a><sup>3</sup>, <a href="http://tianjiashao.com/">Tianjia Shao</a><sup>2</sup>, <a href="https://www.math.ucla.edu/~cffjiang/">Chenfanfu Jiang</a><sup>3</sup>, <a href="https://yangzzzy.github.io/">Yin Yang</a><sup>1</sup>
affiliations:
    University of Utah<sup>1</sup>, Zhejiang University<sup>2</sup>, University of California, Los Angeles<sup>3</sup>
paper: https://arxiv.org/abs/2311.13099
video:  https://fytalon.github.io/pienerf/
code: https://fytalon.github.io/pienerf/
data: 
---


<section class="hero teaser">
<div class="container is-max-desktop">
<div class="hero-body">
<img src="./static/image/teaser.png" class="interpolation-image">
<h2 class="subtitle has-text-centered">
<span class="dnerf">Pie-Nerf</span>🍕 is an efficient and versatile pipeline that synthesizes physics-based novel motions of complex NeRF models interactively. 
</h2>
</div>
</div>
</section>

<div class="columns is-centered has-text-centered">
    <div class="column is-four-fifths">
        <h2>Abstract</h2>
        <div class="content has-text-justified">
We show that physics-based simulations can be seamlessly integrated with NeRF to generate high-quality elastodynamics of real-world objects. Unlike existing methods, we discretize nonlinear hyperelasticity in a meshless way, obviating the necessity for intermediate auxiliary shape proxies like a tetrahedral mesh or voxel grid. A quadratic generalized moving least square (Q-GMLS) is employed to capture nonlinear dynamics and large deformation on the implicit model. Such meshless integration enables versatile simulations of complex and codimensional shapes. We adaptively place the least-square kernels according to the NeRF density field to significantly reduce the complexity of the nonlinear simulation. As a result, physically realistic animations can be conveniently synthesized using our method for a wide range of hyperelastic materials at an interactive rate.
        </div>
    </div>
</div>




---


## Pipeline

![](/pienerf/static/image/pipeline.png)
The input of PIE-NeRF is the same as other NeRF-based frameworks, which consists of a collection of images of a static scene. An adaptive Poisson disk sampling is followed to query the 3D geometry of the model, which are sparsified into n Q-GMLS kernels. Integrator points are placed over the model, including centers of Q-GMLS kernels (i.e., kernel IPs). Discretization at kernels and numerical integration at IPs enable efficient synthesis of novel and physics-based elastodynamic motions. The quadratic warping scheme helps to better retrieve the color/texture of a deformed spatial position to render the final result.



## Interactive showcase


We interact with all types of objects and generat physically realistic dynamic motions.

<div class="columns is-centered">
<div class="column">
<div class="content">
<h4 class="title is-size-5" style="text-align: center;">Dragging excavator </h4>
<video id="dollyzoom" autoplay="" controls="" muted="" loop="" playsinline="" height="100%">
<source src="./static/video/excavator_1.mp4" type="video/mp4">
</video>
</div>
</div>
<div class="column">
<div class="content">
<h4 class="title is-size-5" style="text-align: center;">Dragging ficus tree</h4>
<video id="dollyzoom" autoplay="" controls="" muted="" loop="" playsinline="" height="100%">
<source src="./static/video/ficus_2.mp4" type="video/mp4">
</video>
</div>
</div>
</div>










## Citation
```
@misc{feng2023pienerf,
      title={PIE-NeRF: Physics-based Interactive Elastodynamics with NeRF}, 
      author={Yutao Feng and Yintong Shang and Xuan Li and Tianjia Shao and Chenfanfu Jiang and Yin Yang},
      year={2023},
      eprint={2311.13099},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```
