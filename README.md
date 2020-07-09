# Data set structure
### Example of a data set folder structre 
#### Note: Each element of the list below is a folder

* *InstitutionName* Dataset
  * Objects
    * Boxes
    * ElectricalComponents
    * Humans
  * Scenes
    * Testbench
    * Workcell
      * Synthetic
        * Ideal
        * NoiseModel_A
        * NoiseModel_B
      * Real
        * Sensor_A
        * Sensor_B
      * GroundTruth
        * Synthetic
        * Real
    * Worktable

For each scene/object data set, a common file structure should have the separation of Synthetic and Real, together with the Ground Truth forming one folder level. The sub-level of Synthetic, Real and Ground Truth folder level contains different folders specifying the characteristics of each. 
E.g., the **Synthetic** folder should contain following sub-folders: _Ideal, NoiseModel_A, NoiseModel_B, ..._. The _NoiseMode_A_ folders contains data regarding a specific noise model of a sensor. 
The **Real** folder should contain sub-folders representing different sensors: _Sensor_A, Sensor_B, ..._.

On the elementary level, folders should have the following data: 

1. SceneName_TypeOfData_(NoiseModel_)RGB_index.png _(example: Workcell_Synthetic_Ideal_RGB_1.png)_
2. SceneName_TypeOfData_(NoiseModel_)Depth_index.png _(example: Workcell_Real_SensorB_Depth_48.png)_
3. SceneName_TypeOfData_(NoiseModel_)RGBD_index.png _(example: Workcell_Real_SensorB_RGBD_48.png)_
4. SceneName_TypeOfData_(NoiseModel_)XYZ_index.pcd _(example: Testbench_Synthetic_NoiseModelA_XYZ_432.png)_
5. SceneName_TypeOfData_(NoiseModel_)XYZRGBA_index.pcd _(example: Testbench_Synthetic_NoiseModelA_XYZRGBA_432.png)_

The **GroundTruth** folders should contain following data:

1. SceneName_TypeOfData_GT_index.png _(example: Worktable_Synthetic_GT_2.png)

### Additional information

Every sub-folder (e.g. _Workcell_) should contain a **.txt** describing which data will be used for learning, evaluation and testing.

**All the sub-folders of a specific scene must be there even if they are empty!**
    
# File extensions
### Supported file extensions regarding different data types

1. Image, Depth data: **.png**
2. Ground Truth: **.png**, **.ply**
3. Point Cloud: **.pcd**
