# Optical_Flow_Semantics
## 1. Overview
* PMBP baseline code is mostly borrowed from [https://github.com/fbesse/pmbp](https://github.com/fbesse/pmbp) with slight modification (for compatibility with ubuntu).
* Theretically, our method *Optical flow with semantic infomation* is mostly based on the paper *[Joint Optical Flow and Temporally Consistent
Semantic Segmentation](https://link.springer.com/chapter/10.1007/978-3-319-46604-0_12)* with some simplification.
* Some data is remained in the folder ./devkit, in case someone wants to run the evaluation code directly. The running guidance can be found in [the Appendix Section of our report]()
## 2. Implementation Details
* The overall optical flow estimation program could be devided into four stages, as shown below. For more details, please refer to our report and references.\
![pseudo_code](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/program%20structure.jpg?raw=true)

* The UML diagram of PMBP algorithm is illustrated below.\
![PMBP_UML](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/algorithm_diagram.jpg?raw=true)
* The function call diagram of PMBP algorithm is illustrated below.\
![PMBP_Function_Call](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/FunctionCall.png?raw=true)

## 3. Results
### 3.1 Preprocessing
* Semantic segmentation result. Generated by a FCN neural network.\
![image_segmentation](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/segmented_image.jpg?raw=true)
* Superpixel result. Generated by a python-opencv function.\
![super_pixel](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/superpixel.jpg?raw=true)

### 3.2 Optical Flow
* The input data (one of the image pair)\
![image_dataset](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/000010_10.png?raw=true)
* Baseline result (withour preprocessing information)\
![baseline](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/baseline.jpg?raw=true)
* Our method result (with vectorization speed-up) [parameters need to be tuned]
![fast_result](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/fast.jpg?raw=true)

**Fl**:  Percentage ofoptical flow outliers\
**bg**: Percentage of outliers averaged onlyover background regions\
**fg**: Percentage of outliers averagedonly over foreground regions\
**all**: Percentage of outliersaveraged over all ground truth pixels\
![result_table](https://github.com/panshim/Optical_Flow_Semantics/blob/main/description_docs/result.jpg?raw=true)

## 4. TODO
* The optical flow result of our method is not ideal. Parameters in energy function terms need to be tuned.
* More energy terms mentioned in the reference paper need to be added into our method.
* Gradient descent algorithm needs to be cleaned up.
