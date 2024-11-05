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

# Surface Reconstruction Using Rotation Systems

<font size="4">
<a href="https://cuirq3.github.io/" style="font-size:100%;">Ruiqi Cui<sup>1</sup></a>&emsp;
<a href="https://orbit.dtu.dk/en/persons/emil-toftegaard-g%C3%A6de" style="font-size:100%;">Emil Toftegaard Gæde<sup>1</sup> </a>&emsp;
<a href="http://www2.compute.dtu.dk/~erot/" style="font-size:100%;">Eva Rotenberg<sup>1</sup> </a>&emsp;
<a href="https://www.graphics.rwth-aachen.de/person/3/" style="font-size:100%;">Leif Kobbelt<sup>2</sup> </a>&emsp;
<a href="https://people.compute.dtu.dk/janba/" style="font-size:100%;">J. Andreas Bærentzen<sup>1</sup> </a>&emsp;
</font>
<br>

<font size="4">
<sup>1</sup> Department of Applied Mathematics and Computer Science, Technical University of Denmark, Denmark

<sup>2</sup> Visual Computing Institute, RWTH Aachen University, Germany
</font>

| <a href="https://github.com/cuirq3/RsR">Code</a> | <a href="https://arxiv.org/abs/2402.01893">arXiv</a> | <a href="">Presentation video(TODO, link)</a> |

<img src="./pics/teaser.png" alt="teaser.png"/><img src="./pics/Scene_Stanford.png" alt="stanford.png"/> <br>

</div>

# Abstract

_We propose a combinatorial method for reconstruction of surfaces from points. Our method
constructs a spanning tree and a rotation system. Since the tree is trivially
a planar graph, its rotation system determines a genus zero surface with a
single face which we proceed to incrementally refine by inserting edges to
split faces. In order to raise the genus, special handles are added in a later
stage by inserting edges between different faces and thus merging them. It turns out that our approach has two specific benefits over the other methods. First, the output mesh preserves the
most information from the input point cloud. Second, our method provides
control over the topology of the reconstructed surface._

# Acknowledgments
We thank all data providers: the Stanford Computer Graphics Laboratory; Qingnan Zhou and Alec Jacobson; Chu et al.; Armeni et al.; Matterport, Inc.; Knapitsch et al.; and Anderson Winkler. We thank the anonymous reviewers for their helpful comments. This work is partially supported by a DTU alliance scholarship, the Danish Council for Independent Research (6111-00552B), the Carlsberg Foundation (CF21-0302), and the German Research Foundation (Gottfried Wilhelm Leibniz programme).
# BibTeX

```
@article{cui2024surface,
  title={Surface Reconstruction Using Rotation Systems},
  author={Cui, Ruiqi and G{\ae}de, Emil Toftegaard and Rotenberg, Eva and Kobbelt, Leif and B{\ae}rentzen, J Andreas},
  journal={arXiv preprint arXiv:2402.01893},
  year={2024}
}
```