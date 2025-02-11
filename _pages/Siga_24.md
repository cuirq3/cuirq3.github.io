---
layout: page
title: 
permalink: /projects/siga_24/
nav: false
nav_order: 2
horizontal: false
category: work
---
<div align="center">

<h1>Surface Reconstruction Using Rotation Systems <br> SIGGRAPH ASIA 2024, ACM Transactions on Graphics (TOG)</h1>

<br>
<font size="4">
<a href="https://cuirq3.github.io/" style="font-size:100%;">Ruiqi Cui<sup>1</sup></a>&emsp;
<a href="https://orbit.dtu.dk/en/persons/emil-toftegaard-g%C3%A6de" style="font-size:100%;">Emil Toftegaard Gæde<sup>1</sup> </a>&emsp;
<a href="http://www2.compute.dtu.dk/~erot/" style="font-size:100%;">Eva Rotenberg<sup>1</sup> </a>&emsp;
<a href="https://www.graphics.rwth-aachen.de/person/3/" style="font-size:100%;">Leif Kobbelt<sup>2</sup> </a>&emsp;
<a href="https://people.compute.dtu.dk/janba/" style="font-size:100%;">J. Andreas Bærentzen<sup>1</sup> </a>&emsp;
</font>
<br>
<br>

<font size="4">
<sup>1</sup> Department of Applied Mathematics and Computer Science, Technical University of Denmark, Denmark
<br>
<sup>2</sup> Visual Computing Institute, RWTH Aachen University, Germany
</font>

<br>
<br>
| <a href="https://github.com/cuirq3/RsR">Code</a> | <a href="https://arxiv.org/abs/2402.01893">arXiv</a> | <a href="https://www.bilibili.com/video/BV1HzmrY5E6S/?vd_source=7dd9c5f7c418f642c71d27b55fac942e">Bilibili</a> |

<br>
<br>

<iframe width="560" height="315" 
        src="https://www.youtube.com/embed/9DEfhN3pzng" 
        frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
</iframe>
<br>
<br>


<img src="../../assets/img/Siga_24/teaser.png" alt="teaser.png" style="max-width: 100%; height: auto;"/><br>
<p style="text-align: left;"><b>Fig. 1.</b> Reconstruction process of a high-genus shape. Starting from the point cloud, a minimum spanning tree (MST) is built. By iteratively inserting proper edges into the MST while keeping the genus to zero, a mesh is provided with multiple cracks. Later, with the red edges connecting both sides of the cracks, the genus number of the mesh is increased. Finally, this convoluted high-genus shape is well reconstructed.</p>

</div>

### Abstract

_We propose a combinatorial method for reconstruction of surfaces from points. Our method
constructs a spanning tree and a rotation system. Since the tree is trivially
a planar graph, its rotation system determines a genus zero surface with a
single face which we proceed to incrementally refine by inserting edges to
split faces. In order to raise the genus, special handles are added in a later
stage by inserting edges between different faces and thus merging them. It turns out that our approach has two specific benefits over the other methods. First, the output mesh preserves the
most information from the input point cloud. Second, our method provides
control over the topology of the reconstructed surface._

<div align="center">
<img src="../../assets/img/Siga_24/pipeline_v2.png" alt="pipeline.png" style="max-width: 100%; height: auto;"/><br>
<p style="text-align: left;"><b>Fig. 2.</b> Pipeline overview on synthetic letter point clouds. High-genus reconstruction follows the bottom pipeline, where 𝑔 stands for the genus number. Given the prior knowledge of a genus-0 shape, the shorter pipeline depicted at the top is employed. In the pipeline shown at the bottom, the red edges in the third inset denote the newly added handles. Concurrently, the path formed by the blue edges represents the shortest path between the two end vertices before the red edge is introduced.
</p>
<br>
<br>

<img src="../../assets/img/Siga_24/Scene_Stanford.png" alt="stanford.png" style="max-width: 100%; height: auto;"/>
<img src="../../assets/img/Siga_24/Scene_Synth1.png" alt="synth.png" style="max-width: 100%; height: auto;"/>
<img src="../../assets/img/Siga_24/Scene_Scans.png" alt="scan.png" style="max-width: 100%; height: auto;"/><br>

<p style="text-align: left;"><b>Fig. 3.</b> Renderings of models reconstructed using our method. Top image: well-known models from the Stanford 3D Scanning Repository. Middle image: several test objects are shown. The terrain (shown after hole closing) consists of two very close surfaces, the tree exhibits significant variation point density, and the two remaining objects are high-genus shapes. Bottom: we used our method to reconstruct the DTU STL0024 model as well as the Stanford Armadillo and Bunny directly from the acquired points. For each model, we see unprocessed reconstructions on the left and models after hole closing and denoising on the right. In all images, back-facing surfaces are rendered in red to show holes in the reconstruction.
</p>
<br>
<br>

<img src="../../assets/img/Siga_24/synthetic_general_v2.png" alt="syn_g.png" style="max-width: 100%; height: auto;"/><br>
<p style="text-align: left;"><b>Fig. 4.</b> Visualization of the reconstruction results from six different methods on special synthetic data. A detailed image enclosed by red dashed lines indicates the best reconstruction outcome.
</p>
<br>
<br>

<img src="../../assets/img/Siga_24/real_scan_general_v2.png" alt="scan_g.png" style="max-width: 100%; height: auto;"/><br>
<p style="text-align: left;"><b>Fig. 5.</b> This is the visualization of the reconstruction results by five different methods. It can be noticed that ours, ScaleSpace, Co3Ne w/ smoothing, and Screened Poisson successfully reconstruct reasonable meshes of the input point cloud. Comparing ours and ScaleSpace, our method can reconstruct a more complete mesh with a smaller number of holes while ScaleSpace is restricted by the parameter of the Ball-Pivoting algorithm.
</p>
<br>
<br>

<img src="../../assets/img/Siga_24/topo_control.png" alt="topo.png" style="max-width: 100%; height: auto;"/><br>
<p style="text-align: left;"><b>Fig. 6.</b> Reconstruction comparisons using a synthetic cortical surface point cloud. Our method successfully generated a genus-0 mesh, whereas Co3Ne retained only one side of the compressed opposite points, and Scalespace formed bridges across the gap.
</p>
<br>
<br>

</div>


### Acknowledgments
We thank all data providers: the Stanford Computer Graphics Laboratory; Qingnan Zhou and Alec Jacobson; Chu et al.; Armeni et al.; Matterport, Inc.; Knapitsch et al.; and Anderson Winkler. We thank the anonymous reviewers for their helpful comments. This work is partially supported by a DTU alliance scholarship, the Danish Council for Independent Research (6111-00552B), the Carlsberg Foundation (CF21-0302), and the German Research Foundation (Gottfried Wilhelm Leibniz programme).

### BibTeX

```
@article{10.1145/3687956,
author = {Cui, Ruiqi and G\ae{}de, Emil Toftegaard and Rotenberg, Eva and Kobbelt, Leif and B\ae{}rentzen, J. Andreas},
title = {Surface Reconstruction Using Rotation Systems},
year = {2024},
issue_date = {December 2024},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
volume = {43},
number = {6},
issn = {0730-0301},
doi = {10.1145/3687956},
journal = {ACM Trans. Graph.},
month = nov,
articleno = {190},
numpages = {22},
keywords = {triangle mesh, surface reconstruction, point cloud, graph}
}

```