#   DeTraC_COVId19

##        DeTraC COVID-19 classification in chest X-ray images 

*Asmaa Abbas, Mohammed M. Abdelsamea, Mohamed Medhat Gaber21Mathematics **"Classification of COVID-19 in chest X-ray images usingDeTraC 
deep convolutional neural network"**,2020*

### Motivation
 Here, we validate and adopt our deep CNN approach, called Decompose, Transfer, and Compose (DeTraC), for the classification of COVID-19 chest X-ray images. DeTrac has achieved a high accuracy of 95.12% (with sensitivity of 97.91%, specificity of 91.87%, and precision of 93.36%) in the detection of COVID-19 X-ray images from normal, and severe acute respiratory syndrome cases. 
 
 
## **Dataset description**

We used **80** samples of normal CXRs from the Japanese Society of Radiological Technology and the following open source chest radiography datasets, which contains **105** and **11** samples of COVID-19 and SARS (with 4248×3480 pixels).


```python
open source for chest radiography datasets:
 https://github.com/ieee8023/covid-chestxray-dataset
```
## **Requirement**

Matlab R2019a - window 8 or later version

## A guidance for usage

1. Consist of three parts :
- Run (Training_original_classes.m) matlab file on the original classes (dataset A),
- check the validation accuracy to get the significant classification performence ,
- using the learned weights to get the features for each class separetly.
2. Run (Pca_CXR.m) matlab file to reduce the dimension features space for each original class.
3. Run (construct_dataset_B.m) to apply the K-means clustering algorithm.
4. Run (Training_after_decompose.m) to apply the DeTraC model.

## **Results**

DeTraC_COVID19 achieved high accuracy of 95.12% which proved that CNNs have an effective and robust solution for the detection 
of the COVID-19 cases from CXR images and as a consequence this can be contributed to control the spread of the disease.


**Table 1:** the samples distribution in each class of chest X-ray dataset before and after class decomposition.

<table>
  <tr>
    <th>Original <br>Labels</th>
    <th colspan="2">normal</th>
    <th colspan="2">COVID_19</th>
    <th colspan="2">SARS</th>
  </tr>
  <tr>
    <td># instances</td>
    <td colspan="2">80</td>
    <td colspan="2">105</td>
    <td colspan="2">11</td>
  </tr>
  <tr>
    <td>Decomposed<br>Labels</td>
    <td>norm_1</td>
    <td>norm_2</td>
    <td>COVID19_1</td>
    <td>COVID19_2</td>
    <td>SARS_1</td>
    <td>SARS_2</td>
  </tr>
  <tr>
    <td># instances</td>
    <td>441</td>
    <td>279</td>
    <td>666</td>
    <td>283</td>
    <td>63</td>
    <td>36</td>
  </tr>
</table>

**Table 2:** COVID-19 classification obtained byDeTraC-ResNet18on chest X-rayimages.
|  Accuracy | Sensitivity  |  Specificity |  Precision |
| ------------ | ------------ | ------------ | ------------ |
|  95.12%      | 97.91%      |      91.87%  |  93.36% |

 Fig: the learning curve accuracy and loss between training and test sets.

![1](https://github.com/asmaa4may/DeTraC_COVId19/blob/master/images/Learning%20curve.png ) 


## Contact
Please do not hesitate to contact us if you have any question. 

## Citation

 If you used DeTraC and found it useful, please cite the following papers:
 
*Asmaa Abbas, Mohammed M. Abdelsamea, Mohamed Medhat Gaber21Mathematics **"Classification of COVID-19 in chest X-ray images usingDeTraC 
deep convolutional neural network"**,2020*

•	Abbas A, Abdelsamea MM, Gaber MM. **"Classification of COVID-19 in chest X-ray images usingDeTraC deep convolutional neural network. under review"**, 2020.

 
## License
[MIT](https://github.com/asmaa4may/DeTraC_COVId19/blob/master/LICENSE)





