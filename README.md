# semantic-segmentaion-water-bodies


- *Introduction:*
    - Problem Statement: Unveiling water bodies from satellite images using semantic segmentation for applications in environmental monitoring, urban planning, and more.
    - Objective: Utilize advanced semantic segmentation techniques to achieve high accuracy, with a focus on maximizing the Intersection over Union (IoU) score.
    - Why do we want to unveil water bodies using segmentation?
        - Water Body Mapping & Monitoring: allows for the precise water body identification and delineation
        - Water Quality Assessment: identify areas with different water quality characteristics, like turbidity or pollution levels
        - Change Detection: Tracks changes in water extent, shoreline erosion, and new water bodies by comparing segmented images over time
- *Results:*
    -  Custom U-Net IoU Score: Achieved an IoU of 0.810 with the custom U-Net model.
    -  U-Net with ResNet101 IoU Score: Improved IoU to 0.828 by incorporating ResNet101.
    -  DeepLabv3 IoU Score: Attained a competitive IoU of 0.825 with DeepLabv3.
    -  Comparison Charts: Included charts comparing the IoU scores and Dice loss of different models.

  ![alt text](https://github.com/lalwanii26/semantic-segmentaion-water-bodies/blob/main/images/result.png?raw=true)

- *Evaluation Metrics:*

  ![alt text](https://github.com/lalwanii26/semantic-segmentaion-water-bodies/blob/main/images/evaluation%20metrics.png?raw=true)

- *Visualizations:*
  - Segmented Images: Showcased the segmented images alongside original and ground truth images for all models.
  
    ![alt text](https://github.com/lalwanii26/semantic-segmentaion-water-bodies/blob/main/images/visualization.png?raw=true)

- *Conclusion and Future Work:*

- *Conclusion and Future Work:*
  - U-Net performs better (ideally) than FCN, PSPNet and DeepLab due to the presence of skip connections between the encoder-decoder model.
  - Deep Lab is expected to perform better if we use the actual Deep Lab Model instead of deeplabv3_mobilenet_v3_large.
  - Equipping models with a pre-trained backbone like ResNet or VGG gives better performance.
  - Pre-trained backbones can make the model memory-heavy, and for a simpler use-case like binary semantic-segmentation, a distilled down version makes more sense.
  - We are currently optimizing our custom U-net (which is lighter) and trying to make it perform better by incorporating channel attention and leaky ReLU.

- More details are mentioned in the `slides/Semantic_Segmentation_of_Water_Bodies.pdf`
