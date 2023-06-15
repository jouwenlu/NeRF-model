# NeRF-model
Built a NeRF (Neural Radiance Field) neural network, which constructs novel views of 3D scenes given 2D images with partial views.

*Note: This is an individual project in a Machine Perception class. 

### Work Done

#### Part 1: Fitting a 2D Image
We constructed a simple multilayer perception with 3 linear layers, with ReLU and sigmoid activation functions. With positional encoding, we an image to the model, so that the model represents the Starry Night image. 


#### Part 2: Fitting a 3D Image (NeRF-model)

We constructed a multilayer perception with 10 fully-connected layers, with ReLU and and sigmoid activation functions. The neural network takes in a position (x, y, z), a sample point on a ray, and returns a color and density value. We train the model with positional encoding on a set of 2D images of a lego tractor with their corresponding camera poses. We compute camera rays from the camera, sample 3D points along these rays, and feed them into the network. The returned RBG and density values are used to compute an image with volumetric rendering and its corresponding pose. The loss is calculated by comparing the predicted image with the given image. After training the neural network, it can return a rendered novel 2D view of the scene with a given new pose. 
