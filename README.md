# Tennis Like the Tennis Pros (Forehand Swing)

## Abstract
While tennis research and analytics is a developing field, it has yet to penetrate the professional 
world in a way that is noticeable to the everyday fan nor is it easily accessible to the recreational 
player. This project uses available open-source software, such as OpenPose, for the purpose of 
tracking movement of various tennis professionals during play. While the proposal includes 
features such as court movement and shot selection, this project focuses on forehand arm 
angle as a proof of concept. Thereafter, recreational users can be matched with a professional 
that the user’s play is most similar to in order to provide the user a better frame of reference for 
which professional the user should study further. This project hopes to better bridge the gap 
between recreational players and their favorite professional players as well as provide an 
avenue for the growth in tennis analytics.

Keywords: tennis, forehand, pose estimation, computer vision, analytics


## Navigation
### Primary Material
* To access the full detailed conference paper, review [Tennis Like the Tennis Pros (Forehand Swing) - Eric Li.pdf](https://github.com/itstooerli/tennis-analysis/blob/main/Tennis%20Like%20the%20Tennis%20Pros%20(Forehand%20Swing)%20-%20Eric%20Li.pdf)
* To access the video summary, review [ericLi_analytics_29.mp4](https://github.com/itstooerli/tennis-analysis/blob/main/ericLi_analytics_29.mp4)
* To access the related presentation as a PDF, review [Presentation - Swing Like the Tennis Pros.pdf](https://github.com/itstooerli/tennis-analysis/blob/main/Presentation%20-%20Swing%20Like%20the%20Tennis%20Pros.pdf)
* To access the related presentation as a PowerPoint presentation, review [Presentation - Swing Like the Tennis Pros.pptx](https://github.com/itstooerli/tennis-analysis/blob/main/Presentation%20-%20Swing%20Like%20the%20Tennis%20Pros.pptx)
* To access the initial data compilation, review [FinalProject_Data_Compilation.ipynb](https://github.com/itstooerli/tennis-analysis/blob/main/FinalProject_Data_Compilation.ipynb). Note this notebook requires a properly equipped GPU, which is why it is run on Google Colab.
* To access the project analysis code, review [ProjectAnalysis.ipynb](https://github.com/itstooerli/tennis-analysis/blob/main/ProjectAnalysis.ipynb)
* To access the project analysis code as HTML for browser, review [ProjectAnalysis.html](https://github.com/itstooerli/tennis-analysis/blob/main/ProjectAnalysis.html)

### Supplemental Material
* The OpenPose .mp4 files are located in the ./videos/ directory
* The OpenPose .json files are located in the ./pose_output/ directory

## Findings and Discussion
(I recognize that the facecolor of the plot axes may blend on dark mode. I fill fix on a future iteration of this README.me. For a closer look, please review the provided report/notebook.)

![rog_fed_openpose_example](/images/rog_fed_openpose_example.png)

![nov_djo_openpose_example](/images/nov_djo_openpose_example.png)

With the compilation of arm angle per frame for each of the ten clips chosen, we can assess each players’ peak arm angle during his forehand. Figure 7 shows the arm angle progression for Roger Federer for each of his clips. Figure 8 shows the arm angle progression for Novak Djokovic for each of his clips. Roger Federer, with a known straight arm forehand technique, has a notable peak when performing his forehand. Novak Djokovic, with a known bent arm forehand technique, has a less pronounced peak when completing his forehand. Due to the variance in clip length and frames per second, the most comparable point of interest is the peak arm angle for each of the frames during the player’s forehand. When averaged together, Roger Federer has a mean peak arm angle of 165 degrees, while Novak Djokovic has a mean peak arm angle of 151 degrees. These values confirm our understanding of each player’s forehand technique, discussed earlier.

![rog_fed_peak_arm_angle](/images/rog_fed_peak_arm_angle.png)

![nov_djo_peak_arm_angle](/images/nov_djo_peak_arm_angle.png)

Finally, we compare the arm angle progression for the novice recreational player to match the recreational player to a professional player. Figure 9 shows the arm angle progression for the recreational player. This player’s mean peak arm angle was 146 degrees. Therefore, we would conclude that this player has a bent arm forehand technique that more closely matches Novak Djokovic’s 151 degree mean peak arm angle as compared to Roger Federer’s 165 degree mean peak arm angle. The player can leverage this information from this analysis by studying more of Novak Djokovic’s forehand rather than focus on Roger Federer’s different technique.

![user_peak_arm_angle](/images/user_peak_arm_angle.png)

## Limitations and Future Work
As an isolated proof of concept, this project did have noteworthy limitations. The design methodology required manual work to isolate the player of interest in the clips. To improve on this limitation, we would spend more time on developing stronger heuristics to allow for more automatic capture of the person of interest. Similarly, we needed to manually distinguish the players’ arm during their forehand swing from the rest of the player’s pose. To improve on this limitation, we would include ball tracking into the methodology to better capture the time of contact with the ball. Next, the professional player database only included two professional players. While these two players were chosen for their difference in arm angle, a larger database would be more helpful for recreational users. Similarly, we would improve upon the user interactivity and usability of such a software to allow users to upload videos and, as necessary, clip the video themselves. Finally, in line with the project premise, this project should be expanded to include other components of a player’s profile, such as movement, posture, contact angle, shot selection, and serve mechanics, to better match the recreational player with an appropriate professional player.

## Authors

Contributors names
* Eric Li

## Acknowledgments

* Credit to CMU Computing Lab for developing the OpenPose software: [GitHub](https://github.com/CMU-Perceptual-Computing-Lab/openpose).