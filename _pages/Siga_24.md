---
layout: page
title: 
permalink: /projects/siga_24/
nav: false
nav_order: 2
horizontal: false
category: work
---
<div class="detail_ct">
        <h2 class="rd_title">Surface Reconstruction Using Rotation Systems</h2>
        <p class="td_text"></p>
        <div class="rd_ct"><p font-size:12px="" style="text-align: center;"><span style="font-size:18px;"><span style="font-family:Arial,Helvetica,sans-serif;">ACM Transactions on Graphics (Proceedings of SIGGRAPH Asia 2024)</span></span></p>

        <p font-size:12px="" style="text-align: center;"><span style="font-family:Arial,Helvetica,sans-serif;"><strong><span style="font-size:14px">​</span></strong></span></p>

<p font-size:12px="" style="text-align: center;"><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">Yilin Liu<sup>1</sup>&nbsp;&nbsp;&nbsp;&nbsp;Ruiqi Cui<sup>1</sup>&nbsp;&nbsp;&nbsp;&nbsp;<a data-ke-src="https://vcc.tech/~kexie" href="https://vcc.tech/~kexie" target="_blank">Ke Xie</a><sup>1</sup>&nbsp;&nbsp;&nbsp;&nbsp;<a data-ke-src="http://socs.uoguelph.ca/~minglun/" href="http://socs.uoguelph.ca/~minglun/" target="_blank">Minglun Gong</a><sup>2</sup>&nbsp;&nbsp;&nbsp;&nbsp;<a data-ke-src="https://vcc.tech/~huihuang" href="https://vcc.tech/~huihuang" target="_blank">Hui Huang</a><sup>1*</sup></span></span></p>

<p font-size:12px="" style="text-align: center;"><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;"><sup>1</sup>Shenzhen University&nbsp; &nbsp;&nbsp;<sup>2</sup>University of Guelph</span></span></p>

<p font-size:12px="">&nbsp;</p>

<p font-size:12px=""><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1651222316692.png"><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1659083784725.png"></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">Fig. 1. Given an unknown large-scale urban site with arbitrary boundary shape (red polygon shown on left), our algorithm designs an aerial flight trajectory in real-time, which guides a single-camera UAV to both explore the site (trajectory shown in yellow) and observe all buildings (trajectory shown in blue). 9,148 images were captured, which support high-quality reconstruction of this 1.35km<sup>2</sup>&nbsp;area through available multi-view stereo matching techniques (right).</span></span></p>

<p font-size:12px="">&nbsp;</p>

<p font-size:12px=""><span style="font-size:18px;"><span style="font-family:Arial,Helvetica,sans-serif;"><strong>Abstract</strong></span></span></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">Existing approaches have shown that, through carefully planning flight trajectories, images captured by Unmanned Aerial Vehicles (UAVs) can be used to reconstruct high-quality 3D models for real environments. These approaches greatly simplify and cut the cost of large-scale urban scene reconstruction. However, to properly capture height discontinuities in urban scenes, all state-of-the-art methods require prior knowledge on scene geometry and hence, additional prepossessing steps are needed before performing the actual image acquisition flights. To address this limitation and to make urban modeling techniques even more accessible, we present a real-time explore-and-reconstruct planning algorithm that does not require any prior knowledge for the scenes. Using only captured 2D images, we estimate 3D bounding boxes for buildings on-the-fly and&nbsp;use them to guide online path planning for both scene exploration and building observation. Experimental results demonstrate that the aerial paths planned by our algorithm in real-time for unknown environments support reconstructing 3D models with comparable qualities and lead to shorter flight air time.</span></span></p>

<p font-size:12px="">&nbsp;</p>

<p font-size:12px=""><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1651222337683.png"><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1659083809455.png"></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">Fig. 2. Overview: Taking the live feed video from a UAV on an appointed site as input, our system detects buildings and estimates their bounding boxes (e.g., the first model in the top row), which guide the UAV to further explore the site (yellow trajectory) and observe buildings from different perspectives (blue trajectory). Additional observations further enhance our knowledge on this site, allowing more buildings being detected and modeled as boxes (remaining models in the top row). At the end of the flight, the captured image sequence (middle) is used to build a high-quality model for the whole scene (bottom).</span></span></p>

<p font-size:12px="">&nbsp;</p>

<p font-size:12px=""><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1651222384273.png"><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1659083824774.png" style="width: 1300px; height: 196px;"></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">Fig. 4. The proposed Region-Division method for global scene exploration. a): At the beginning, the UAV only knows the boundary of the whole area. A (green) region is defined using a default size&nbsp;∈&nbsp;for the UAV to explore. During the exploration, the UAV discovers target building 1, 2, 3 through the perception distance of two cells by default. It switches to reconstruction mode once it arrives at the cells of building 1, 2, but leaves building 3 for the latter processing since it locates outside the green region. b): The target building 3 will guide the formation of the next (blue) region. c): Since no new building is detected during the exploration of the blue region, the next (yellow) region to be explored is defined using size&nbsp;∈&nbsp;again. Buildings 4, 5 detected and reconstructed during the exploration of the yellow region. d): The final path generated by Region-Division divides the whole site into four non-overlapping polygon-shaped regions. It ensures all cells are explored and all buildings are observed. The total path length (22,114) is shorter than the two baselines (Greedy-Nearest: 23,852 and Two-Step: 25,170); see Supplementary for further details.</span></span></p>

<p font-size:12px="">&nbsp;</p>

<p font-size:12px=""><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1651222408608.png"><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1659083838760.png"></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">Fig. 5. Local path planning for target building reconstruction. A set of simple rules are used so that the planning can be done in real-time and adapt to new observations. The trajectories are initialized based on the shape of the building’s bounding box (left) and deformed when the bounding box changes or potential collusion is detected (right).</span></span></p>

<p font-size:12px="">&nbsp;</p>

<p font-size:12px=""><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1651222429699.png"><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1659083859877.png"></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">Fig. 8. We show on the left a real scene referred to as Academic Building. As illustrated, a single 3D orientated bounding box cannot fit the target building tightly and thus may lose many important geometry details especially in the concave areas. On the right, we show an ablation study that uses different trajectories to observe the buildings: a) 80% overlap trajectory with split strategy nicely covers all areas of the buildings and hence produces the best model; b) 80% overlap trajectory without split yields shortest flight path, but the samples are not enough for accurate reconstruction; and c) 60% overlap trajectory with split strategy has similar path length as b), but noticeable better reconstruction result.</span></span></p>

<p font-size:12px="">&nbsp;</p>

<p font-size:12px=""><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1651222882593.png"><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1659083877761.png"></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">Fig. 11. Comparison on flight trajectories and reconstruction results on Academic Building. Our approach achieve similar reconstruction quality as the offline optimization-based approach [Zhou et al. 2020], while using much smoother flight trajectories. Note that the trajectory of Oblique Photography covers a larger area to ensure the sufficient image overlap on buildings near the boundary. This is a default behavior in Dji-Terra.</span></span></p>

<p font-size:12px="">&nbsp;</p>

<p font-size:12px=""><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1651222902546.png"><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1659083897972.png"></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">Fig. 14. Visualizing the trajectories designed by the two baseline approaches and the proposed Region-Division method. Our approach decomposes the scene into non-overlapping regions, which can be handled independently.</span></span></p>

<p font-size:12px="">&nbsp;</p>

<p font-size:12px=""><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1651222923587.png"><img alt="" src="https://vcc-szu.s3.ap-southeast-1.amazonaws.com/1659083915214.png"></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">Fig. 16. Visual comparison with Oblique Photography on a real large-scale Campus scene. Our approach decompose this large (1.35km<sup>2</sup>) and irregular-shaped site into multiple non-overlapping regions (Top-Left). The density of the flight trajectory highly depends on the locations of buildings. The finally reconstructed models are noticeably more detailed than those generated by Oblique Photography.</span></span></p>

<p font-size:12px="">&nbsp;</p>

<p font-size:12px=""><span style="font-size:18px;"><span style="font-family:Arial,Helvetica,sans-serif;"><strong>Acknowledgements</strong></span></span></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">We thank all reviewers for their valuable comments. This work was supported in parts by NSFC (U2001206), Guangdong Talent Program (2019JC05X328), Guangdong Science and Technology Program (2020A0505100064), DEGP Key Project (2018KZDXM058), Shenzhen Science and Technology Program (RCJC20200714114435012, JCYJ20210324120213036), NSERC (293127), National Engineering Laboratory for Big Data System Computing Technology, and Guangdong Laboratory of Artificial Intelligence and Digital Economy (SZ).</span></span></p>

<p font-size:12px="">&nbsp;</p>

<p font-size:12px=""><span style="font-size:18px;"><span style="font-family:Arial,Helvetica,sans-serif;"><strong>Bibtex</strong></span></span></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">@article{DroneFly21,</span></span></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">title={Aerial Path Planning for Online Real-Time Exploration and Offline High-Quality Reconstruction of Large-Scale Urban Scenes},</span></span></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">author={Yilin Liu&nbsp;and&nbsp;Ruiqi Cui&nbsp;and&nbsp;Ke Xie&nbsp;and&nbsp;Minglun Gong&nbsp;and&nbsp;Hui Huang},</span></span></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">journal={ACM Transactions on Graphics (Proceedings of SIGGRAPH Asia)},</span></span></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">volume={40},</span></span></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">number={6},</span></span></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">pages={226:1--226:16},</span></span></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">year={2021},</span></span></p>

<p font-size:12px=""><span style="font-size:14px;"><span style="font-family:Arial,Helvetica,sans-serif;">}</span></span></p>
    </div>
</div>