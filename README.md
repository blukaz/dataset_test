# Data set structure
### Example of a data set file structre

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
    
For each scene/object data set, a common file structure should have the separation of Synthetic and Real, together with the Ground Truth forming one folder level. The sub-level of Synthetic, Real and Ground Truth folder level contains different folders specifying the characteristics of each. E.g., the Synthetic folder should contain following sub-folders: _Ideal, NoiseModel_A, NoiseModel_B, ..._. The _NoiseMode_A_ folders contains data regarding a specific noise model of a sensor. The Real folder should contain     
    
# File extensions
### Supported file extensions regarding different data types

1. Image, Depth data: **.png**
2. Ground Truth: **.png**, **.pcd**, **.ply**
3. Point Cloud: **.pcd**, **.ply**
