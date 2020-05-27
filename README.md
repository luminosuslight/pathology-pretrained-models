# Pre-trained Cell Segmentation Models

Machine Learning models for a fast.ai v1 ResNet18 U-Net CNN, to be used with the tool from pathology-ml-model-training repository. See the to-be-released thesis and paper for details.

## Usage

Copy the models to the server of the tool from the `pathology-ml-model-training` repository. While it is not yet possible to choose external models in the UI (as of May 27th 2020), the feature is planned and meanwhile the model can be hardcoded to be the default model in the server (in `server/main.py`).

For each model `trained_model.pth` and `input/export.pkl` is provided. The first is used for easy inference and the second is provided to be able to use the model for transfer learning and retrain it.

## Instance Segmentation

`a0e6aaa83fb7a50ab5de37faef9fecb7-557c183ee44cafc2bf48a20e24543710` is our best performing model for cell instance segmentation on breast cancer fluorescence images. It was first trained with artificial data and then fine tuned with manual annotations from real images. This model is reffered to as `Model D` in the thesis and the paper.

## Instance Segmenation and Epithelial Classification

`7c0c7084ac8007ab0c24a3ee563e349c-d1902cca8d8c72222dc5315c1411a337-92f2cf69f5abe9ea11c31c03f6d8cb23` is based on the best performing instance segmentation model and was extended with manual annotations to also do classification of each cell into epithelial or not. The classification result is returned in the third channel per pixel. This is the model used for the classification evaluation in the thesis and paper.

