---
layout: project_page
permalink: /pienerf/

title: "PIE-NeRF🍕: Physics-based Interactive Elastodynamics with NeRF"
authors:
    Yutao Feng, Yintong Shang, Xuan Li, Tianjia Shao, Chenfanfu Jiang, Yin Yang 
affiliations:
    University of Utah, University of California, Los Angeles, Zhejiang University
paper: 
video:  https://fytalon.github.io/pienerf/
code: https://fytalon.github.io/pienerf/
data: 
arxiv: https://fytalon.github.io/pienerf/
---

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



*The input of PIE-NeRF is the same as other NeRF-based frameworks, which consists of a collection of images of a static scene. An adaptive Poisson disk sampling is followed to query the 3D geometry of the model, which are sparsified into $n$ Q-GMLS kernels. Integrator points are placed over the model, including centers of Q-GMLS kernels (i.e., kernel IPs). Discretization at kernels and numerical integration at IPs enable efficient synthesis of novel and physics-based elastodynamic motions. The quadratic warping scheme helps to better retrieve the color/texture of a deformed spatial position to render the final result.



## Significance


## Citation
```
@article{
}
```
