# CNN Residual Learning Method for Artifacts and Noise Removal in MRI
6.862 Group7 Project | Team Members: Katherine Li & Ngoc La & Tommy Shi
## Description
Magnetic resonance imaging (MRI) with its non-invasive characteristics is a promising method for studying human organs, diagnosing diseases, and staging. However, MR images are sensitive to noises and artifacts that may hinder image quality and consequently the accuracy of interpretation and analysis. In this project, we would like to propose using machine learning (ML) to improve the quality of MRI through a reduction of Rician noise. Specifically, we used a supervised denoising convolutional neural network model (DnCNN) of 17 layers to learn the noise from 1000 synthetic noisy images, which were generated using a combination of T1-weighted brain MR ground-truth images and a Rician noise model with a random signal-to-noise ratio (SNR) in the range of [10, 20]. The learning model was tested with 743 T1-weighted brain MR images obtained from the same source. Quantitatively, we found the model performed well while training with 1000 epochs, producing an average peak signal-to-noise ratio (PSNR) of 31.20dB and mean squared error (MSE) of 52.24. The block matching and 3D filtering method (BM3D) was implemented to provide a baseline comparison for the results obtained from the DnCNN learning model. Numerical results showed that the DnCNN method performed better compared to BM3D in Rician, Gaussian, and Rayleigh random noise images as well as the validation set of 1734 T2 images. Comparing the restored images with their original ground truth and noise-added versions, we found that DnCNN worked relatively well in removing random noise, but was less effective in addressing other forms of noise such as motion and Gibbs ringing artifact in fetal MR images.

The actual implementation codes for the project can be found in folder **src/denoise_cnn**

