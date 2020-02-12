# Image-Restoration

Algorithm which transforms poor quality JPEGs with writing written over the top of them to high quality images.

Steps followed were:
- Function which takes an high quality image and crappifies it
- Created a Generator: Used U-Net with ResNet arch and Pixel-MSE as loss function
- Created a Critic: Used Binary cross entrophy to classify images whether they are generated images or real images.
- Created a GAN learner using pre-trained Generator and Critic which will train the generator once and then train the critic till it's loss is < 0.5 and then switch back to train generator.
This switching is automatically done by AdaptiveGANSwitcher()


Project is still in progress
and trying to implement a technique explained in “Perceptual losses for real time style transfer and super resolution” paper.
