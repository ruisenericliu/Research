Excited to introduce 3DGUT—a Gaussian Splatting formulation that unlocks support for distorted cameras, including time dependent effects like rolling shutter, while maintaining the benefits of rasterization, rendering at \>250 FPS.
 
Our main idea💡: replace EWA splatting formulation used in 3DGS with Unscented Transform, which instead of approximating the projection function, approximates the 3D Gaussians with a set of sigma points that can be projected exactly and are used to compute the Gaussian projections.
 
⭐ Unscented Transform allows us to seamlessly support various distorted cameras and rolling shutter sensors, without deriving a new Jacobian for each camera model - all we need is the projection model.
 
⭐ Splatting based on Unscented Transform is not only much simpler than EWA splatting, but it also better approximates the Monte Carlo approximation. Especially when the cameras are distorted.
 
⭐ We follow 3DGRT and evaluate the particles in 3D, by locating the point of maximum particle response along each ray. This allows us to completely avoid the backpropagation through the projection operation and aligns our representation with 3DGRT.
 
⭐ By aligning with tracing-based approaches, 3DGUT enables secondary ray tracing for advanced effects like reflections and refractions—merging the best of rasterization and ray tracing into a single framework.
 
⭐ Support for distorted cameras and time-dependent effects is especially important in the fields of robotics and autonomous driving. 3DGUT seamlessly supports these datasets while being much faster than the ray tracing approaches.
 
This is an amazing teamwork with Janick Martinez Esturo, Ashkan Mirzaei, Nicolas Moënne-Loccoz, and Zan Gojcic!
 
🗒️ Project Page : [https://lnkd.in/gkF64BPH](https://lnkd.in/gkF64BPH)  
🗒️ Arxiv: [https://lnkd.in/g9yCjqHS](https://lnkd.in/g9yCjqHS)  
⌨️ Code: Coming soon! Keep an eye out.
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>