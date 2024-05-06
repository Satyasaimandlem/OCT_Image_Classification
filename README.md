# Classification of Drusen, DME and CNV OCT images using Deep Learning algorithms

## Introduction:
In contemporary times, there has arisen a burgeoning apprehension concerning retinal ailments, which have surfaced as a notable public health concern. These maladies progress incrementally and often elude detection due to the absence of overt symptoms. According to National Library of Medicine, 2.2 Million people globally are suffering from Vision Impairments, can grow to 5.4 million by 2050. These disorders can manifest in diverse presentations, primarily impacting visual function. They can afflict any segment of the retina, resulting in visual impairments and, in severe instances, blindness. Examples of retinal disorders encompass diabetic retinopathy, macular pucker, glaucoma, macular hole, age-related macular degeneration, drusen, central serous retinopathy, macular edema, vitreous traction, and abnormalities of the optic nerve.

The human eye is an intricate organ tasked with the process of vision, comprising several constituent elements that collaborate harmoniously to capture and interpret light. Its principal components encompass the cornea, iris, pupil, lens, retina, and optic nerve. Positioned at the posterior aspect of the eye, the retina assumes paramount importance, housing light-sensitive cells known as photoreceptors that transmute light into electrical impulses. Within the retina lies the macula, a diminutive region centrally situated, pivotal in facilitating acute, focal vision vital for tasks such as reading and driving. The retina assumes a pivotal function in receiving and structuring visual stimuli. **Early detection and treatment are essential to prevent vision loss.** 

Optical Coherence Tomography (OCT) stands as a pivotal diagnostic instrument, delivering high-fidelity imaging and precise quantification of retinal layers impacted by pathology. Leveraging light waves, OCT generates cross-sectional retinal images, furnishing intricate details crucial for diagnostic discernment and continual monitoring of retinal and optic nerve alterations over time. This technological advancement assumes paramount significance in ensuring precise diagnosis and optimal selection of therapeutic interventions. Ophthalmologists harness OCT's capabilities to meticulously inspect each stratum of the retina, facilitating mapping and evaluation of their thickness, thereby enhancing diagnostic efficacy. These quantitative metrics not only bolster the diagnostic process but also inform therapeutic strategies for conditions like glaucoma and retinal pathologies. OCT finds utility in diagnosing an array of ocular disorders. Traditional classification methodologies for retinal ailments have exhibited accuracies ranging from 80% to 91%. Consequently, a sophisticated deep learning framework predicated on convolutional neural networks has been devised to enhance the precision of retinal disease classification, particularly in the nascent stages of pathology.


![image](https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/257cf11e-ca19-43ff-a36a-375d38fa2e02)

1. Drusen are small yellow deposits that form under the retina, particularly in the macula. OCT images can clearly show the presence of drusen, helping eye care professionals diagnose age-related macular degeneration (AMD), a leading cause of vision loss in older adults.
2. Diabetic macular edema (DME) is a complication of diabetic retinopathy, a condition that affects people with diabetes. OCT is crucial in diagnosing DME as it can visualize the swelling (edema) in the macula caused by fluid leakage from blood vessels.
3. Choroidal neovascularization (CNV) is a condition where abnormal blood vessels grow beneath the retina. OCT imaging can detect CNV by revealing the presence of these abnormal vessels and any associated fluid or blood leakage.
In summary, OCT plays a crucial role in the diagnosis and management of eye conditions such as drusen, DME, and CNV. By providing detailed images of the retina, OCT helps eye care professionals accurately diagnose these conditions and develop appropriate treatment plans to preserve vision.


<img width="750" alt="image" src="https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/209848c1-0d9a-49c7-b149-cf6c7f877e59">


## Dataset:

The dataset used in this project is obtained from Mendeley(https://data.mendeley.com/datasets/rscbjbr9sj/3) and it contains OCT images of retinas. It consists of a total of **62138 images** , categorized into the following classes:
- CNV (Choroidal Neovascularization)
- DME (Diabetic Macular Edema)
- DRUSEN
- NORMAL

The distribution of data is as below:
1. NORMAL - 26565
2. CNV - 15109
3. DME - 11598
4. DRUSEN - 8866

<img width="900" alt="image" src="https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/d87ef1e2-bb5a-4d5d-90b6-647c7f5d4671">

## Preprocessing steps were undertaken as follows:

1. The images were resized uniformly to dimensions of 256x256 pixels.
2. Subsequently, normalization was applied to scale the pixel values within the range of 0 to 1.
3. Augmentation techniques were employed using the following parameters within the defined data augmentation process:
   - Rotation range: 10 degrees
   - Width shift range: 0.1 (10% of the image width)
   - Height shift range: 0.1 (10% of the image height)
   - Shear range: 0.1 (10% shear intensity)
   - Zoom range: 0.1 (zooming range of 10%)
   - Horizontal flip: Enabled (random horizontal flipping)
   - Vertical flip: Enabled (random vertical flipping)
   - Fill mode: Nearest neighbor interpolation to handle pixel filling near boundaries.


We have tried multiple models as given in the Python file attached to this project.

<img width="650" alt="image" src="https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/dd35ff01-382b-411b-9bed-803f28d0cd7c">

Below CNN model proves to be the best.

<img width="650" alt="image" src="https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/d00cc775-74c5-4aa6-b863-53565493eae5">

<img width="896" alt="image" src="https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/f58dc72c-107b-4690-ab15-736311ac2118">


Contact Information:
•	Satyasai Mandlem(satyasm1@umbc.edu)
•	Hemanth Varma Dantuluri (h167@umbc.edu)
•	Nikitha Guntaka



