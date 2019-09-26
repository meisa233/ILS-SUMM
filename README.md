# ILS-SUMM
This repo contains a python implementation of the paper - "ILS-SUMM: Iterated Local Search for Unsupervised Video Summarization" (under the review of ICLR 2020).  
The main requirements are python 3.6 and [moviepy](https://zulko.github.io/moviepy/install.html). Please install other missing dependencies.

![](Cosmus_Laundromat.gif)  
*A video summary of [Cosmus Laundromat movie](https://www.youtube.com/watch?v=Y-rmzh0PI3c) generated by ILS-SUMM.*  

## Get started
1. Download the code
```bash
git clone https://github.com/ICLR-2020-ILS-SUMM/ILS-SUMM.git
```
2. Copy your video file and the features and durations of the video shots into the data directory. Currently the data directory contains the fetures and durations we use for the Cosmus Laundromat movie.
```bash
cp /<yourdatadir>/{features.npy,shots_durations.npy,yourvideo.mp4} /data/
```

## How to run ILS-SUMM
Run demo.py with the video file name and the allowed summarization ratio as arguments.  
For example, assigning 0.1 to summ_ratio means the maximum length of the summary will be 10% of the full video length.
```bash
python demo.py <video_file_name> <summ_ratio>
```
## Example
For Cosmus Laundromat we get the following results:
```bash
The selected shots are: [  2   6   8  39  42  45  47  50  72  75  77  78  79  88 102]
The achieved total distance is: 20.518
```
To illustrate the solution, the following figure will be automatically saved in the data directory:
![](Solution_Visualization.png)  
The features dimension were reduced to two dimensions using PCA. The point radius is proportional to the shot duration, and blue color denotes the shots that were chosen by ILS-SUMM algorithm.




