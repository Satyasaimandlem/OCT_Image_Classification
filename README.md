# OCT_Image_Classification Of Drusen, DME and CNV

Introduction:
In recent times, there has been a growing concern regarding retinal disorders, which have emerged as a significant public health issue. These disorders progress gradually and often go unnoticed without any apparent symptoms. Each year, millions of individuals worldwide receive a diagnosis of a retinal condition. These disorders can manifest in various forms, most commonly affecting vision. They can affect any part of the retina, leading to visual impairments, and in severe cases, blindness. Examples of retinal disorders include diabetic retinopathy, macular pucker, glaucoma, macular hole, age-related macular degeneration, drusen, central serous retinopathy, macular edema, vitreous traction, and optic nerve abnormalities.

The human eye is a complex organ responsible for vision, composed of several parts that work together to capture and process light. The main components of the eye include the cornea, iris, pupil, lens, retina, and optic nerve.The retina is a crucial part of the eye located at the back, containing light-sensitive cells called photoreceptors that convert light into electrical signals. The macula is a small area in the center of the retina responsible for sharp, central vision, essential for activities like reading and driving. Retina plays a crucial role in receiving and organizing visual information. **Early detection and treatment are essential to prevent vision loss.** 

Optical Coherence Tomography (OCT) is a diagnostic tool that provides high-resolution imaging and quantification of retinal layers affected by disease. OCT uses light waves to capture cross-sectional images of the retina, providing detailed information for diagnosis and monitoring changes in the retina and optic nerve over time. This technology is crucial for accurate diagnosis and selection of appropriate treatment options. Ophthalmologist can use OCT to observe each of the retina's different layers. Ophthalmologist will be able to map and assess their thickness as a result of this. These metrics aid in the diagnosing process. They also offer medical advice for glaucoma and retinal problems. OCT may be used to diagnose a variety of eye disorders.Traditional methods of classifying retinal disorders have shown an accuracy ranging from 80% to 91%. Therefore, a deep learning system based on convolutional neural networks has been developed to classify retinal diseases more accurately, particularly in the early stages.
![image](https://github.com/Satyasaimandlem/OCT_Image_Classification/assets/129209796/83cb61d2-b7d4-4942-bd86-b919160fcf77)

1. Drusen are small yellow deposits that form under the retina, particularly in the macula. OCT images can clearly show the presence of drusen, helping eye care professionals diagnose age-related macular degeneration (AMD), a leading cause of vision loss in older adults.
2. Diabetic macular edema (DME) is a complication of diabetic retinopathy, a condition that affects people with diabetes. OCT is crucial in diagnosing DME as it can visualize the swelling (edema) in the macula caused by fluid leakage from blood vessels.
3. Choroidal neovascularization (CNV) is a condition where abnormal blood vessels grow beneath the retina. OCT imaging can detect CNV by revealing the presence of these abnormal vessels and any associated fluid or blood leakage.
In summary, OCT plays a crucial role in the diagnosis and management of eye conditions such as drusen, DME, and CNV. By providing detailed images of the retina, OCT helps eye care professionals accurately diagnose these conditions and develop appropriate treatment plans to preserve vision.

![image](https://github.com/Satyasaimandlem/OCT_Image_Classification/assets/129209796/d5d22713-41ae-4b09-b7c3-e8a95a5883ff)

Dataset:

The dataset used in this project is obtained from Mendeley(https://data.mendeley.com/datasets/rscbjbr9sj/3) and it contains OCT images of retinas. It consists of a total of 62138 images, categorized into the following classes:
- CNV (Choroidal Neovascularization)
- DME (Diabetic Macular Edema)
- DRUSEN
- NORMAL

Distribution of data is as below:
CNV :15109
DME :11598
DRUSEN: 8866
NORMAL: 26565

![image](https://github.com/Satyasaimandlem/OCT_Image_Classification/assets/129209796/bdfdc494-ba14-478b-878a-d0f60077e6fb)

Preprocessing:
1. We resized the images to 256x256.
2. And normalized images to 0,1
3. Augmentation with below metrics:
   # Define data augmentation
datagen = ImageDataGenerator(
    rotation_range=10,
    width_shift_range=0.1,
    height_shift_range=0.1,
    shear_range=0.1,
    zoom_range=0.1,
    horizontal_flip=True,
    vertical_flip=True,
    fill_mode='nearest'
)



We have tried multiple models as give in the python file atatched to this project.
![image](https://github.com/Satyasaimandlem/OCT_Image_Classification/assets/129209796/8e2132f2-e8f6-4888-974f-39373bfefb76)

Below CNN model proves to be the best.

![image](https://github.com/Satyasaimandlem/OCT_Image_Classification/assets/129209796/e7ca4a24-c44c-4408-80aa-88d06e0c9441)

![image](https://github.com/Satyasaimandlem/OCT_Image_Classification/assets/129209796/29a7c08c-2221-42a7-a921-4068da6872be)




Contact Information:
•	Satyasai Mandlem(satyasm1@umbc.edu)
•	Nikitha Guntaka
•	Hemanth Varma Dantuluri



