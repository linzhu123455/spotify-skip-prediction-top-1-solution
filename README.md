# Our Codes for the WSDM Cup Skip Prediction Challenge (1st Position on the Final Leaderboard)

 

This repository contains the **Python** source code of our solutions to the WSDM Cup 2019.



## Instructions for Running the Code

### Data Preparation

- Firstly, create three folders `train_fold`, `test_fold`, and `Skip_Data`, and put the decompressed train csv files, test csv files, and song feature files there;
- Create a new folder `test_pred`  for storing the processed test files
- Run the `Spotify_Skip_Final_Solution_Data_Preparation` script, note that this script consists of 4 segments, before running the 4th segment, please use the official Glove code at https://github.com/stanfordnlp/GloVe for learning the embeddings from the `glove_data.txt` file generated in previous steps. Glove training parameters are`VOCAB_MIN_COUNT=7`, `VECTOR_SIZE=150`, `MAX_ITER=150` ,`WINDOW_SIZE=10`. This part is quite time consuming, so you may also access the trained embedding from: https://pan.baidu.com/s/1bhJbsGSD7bXf4txmsqaplA

### Model Fitting

Create a new folder `Data` for storing trained model. Run the `Spotify_Skip_Final_Solution_Model_Fitting` script.

### Submission Generation

Run the `Spotify_Skip_Final_Solution_Test_File_Prediction` and then the `Spotify_Skip_Final_Solution_Submission_Generation` scripts. The generated submission file should score 0.648 and achieve top 1 on the leaderboard. To match the 0.651 result, you may only need to train the model 5-6 times, and then average/ensemble the prediction results (Our actual ensembling approach used 6 slight modifications of the core model defined in `Spotify_Skip_Final_Solution_Model_Fitting` script, for example by replacing ReLU activations with ELU activations. But such modifications may not be necessary. Please contact me if you need exact definitions of these model variants).

## License


Copyright [2019][Lin Zhu]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.



## Contact


Our scripts are a little messy and we think there must be some potential mistakes in our codes.
Please feel free to contact us, if there are any question about our project or suggestion to help improve.
email: 371795633@qq.com
