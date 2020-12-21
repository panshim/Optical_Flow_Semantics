# Optical_Flow_Semantics
## 1. Overview
* PMBP baseline code is mostly borrowed from [https://github.com/fbesse/pmbp](https://github.com/fbesse/pmbp) with slight modification (for compatibility with ubuntu).
* Theretically, our method *Optical flow with semantic infomation* is mostly based on the paper *[Joint Optical Flow and Temporally Consistent
Semantic Segmentation](https://link.springer.com/chapter/10.1007/978-3-319-46604-0_12)* with some simplification.
* Some data is remained in the folder ./devkit, in case someone wants to run the evaluation code directly. The running guidance can be found in [the Appendix Section of our report]()
## 2. Implementation Details
* The overall optical flow estimation program could be devided into four stages, as shown below. For more details, please refer to our report and references.\
![pseudo_code](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/program%20structure.jpg?raw=true)

* PMBP algorithm is 
![PMBP_UML](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/algorithm_diagram.jpg?raw=true)

## 3. Results
### 3.1 Preprocessing
![image_segmentation](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/segmented_image.jpg?raw=true)

![super_pixel](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/superpixel.jpg?raw=true)

### 3.2 Optical Flow
![image_dataset](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/000010_10.png?raw=true)

![baseline](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/baseline.jpg?raw=true)

![fast_result](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/fast.jpg?raw=true)

**Fl**:  Percentage ofoptical flow outliers\
**bg**: Percentage of outliers averaged onlyover background regions\
**fg**: Percentage of outliers averagedonly over foreground regions\
**all**: Percentage of outliersaveraged over all ground truth pixels\
![result_table](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/result.jpg?raw=true)

## 4. TODO

