

Line detection is widely used in many robotic tasks such as scene recognition, 3D reconstruction, and simultaneous localization and mapping (SLAM). Compared to points, lines can provide both low-level and high-level geometrical information for downstream tasks. In this paper, we propose a novel edge-based line detection algorithm, AirLine, which can be applied to various tasks. In contrast to existing learnable endpoint-based methods which are sensitive to the geometrical condition of environments, AirLine can extract line segments directly from edges, resulting in a better generalization ability for unseen environments. Also to balance efficiency and accuracy, we introduce a region-grow algorithm and local edge voting scheme for line parameterization. To the best of our knowledge, AirLine is one of the first learnable edge-based line detection methods. Our extensive experiments show that it retains state-of-the-art-level precision yet with a $3-80\times$ runtime acceleration compared to other learning-based methods, which is critical for low-power robots.

<figure>
    <img src="/img/cp2.png" />
    <figcaption>
        A qualitative comparison across difference methods on untrained samples.
    </figcaption>
    
</figure>
# Methodology
</figure>
    <img src="/img/pipeline.png" />
    <figcaption>
        Pipeline of Airline
    </figcaption>


</figure>

As shown above, AirLine is a learnable edge-based line detection architecture that is composed of four modules including edge detection, orientation detection, conditional region-grow, and line parameterization. We next present their motivation and detailed process, respectively. We made a video to demonstrate each stage.

<figure>
    <img src="/img/pipeline.gif"/>
</figure>

The feature adjacency is established via feature cross-correlation between <img src="https://render.githubusercontent.com/render/math?math=a"> and its neighbors <img src="https://render.githubusercontent.com/render/math?math=\mathcal{N}(a) = \{a, b, c, d, e\}"> to model feature “interaction.”  This makes the lifelong learning techniques for CNN applicable to GNN, as the new nodes in a regular graph become individual training samples.

<figure>
    <figcaption>
        The relationship of a graph and feature graph.
    </figcaption>
    <img src="/img/posts/2022-03-05-lgl/relationship.jpg"/>
</figure>

## Video

{% youtube EKDx3Z9qYUQ %}

## Source Code

* **[Lifelong Graph Learning (Citation Graph)](https://github.com/sair-lab/AirLine)**

## Publications
