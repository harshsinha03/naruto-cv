# Naruto Character Recognition and Analysis

Given a scene from an episode of *Naruto*, track major character's faces, and identify the symbol on their headband.

<img src="http://i.imgur.com/70KWWkZ.png" alt="drawing" width="300"/>

### Source Clips
Some example clips we're planning to be able to run on:
 - [Naruto Shippuden Opening 18](https://www.youtube.com/watch?v=HdgD7E6JEE4)
 - [Naruto Opening 2](https://www.youtube.com/watch?v=SRn99oN1p_c)
 - [Naruto and Hinata Wedding](https://www.youtube.com/watch?v=BoMBsDIGkKI)


### Tasks
- [ ] Create a dataset of character faces with tags, pulling character images from [Jikan](https://jikan.moe/), and cropping faces using the detector [lbpcascade_animeface](https://github.com/nagadomi/lbpcascade_animeface) (Note: this detector will only be used during the generation of the dataset, and only to crop faces). 
   - If more character pictures are needed, we’ll manually pick them to be added from Google Images.
- [ ] Train a network with the created dataset to detect and classify character faces.
  - [ ] Draw a bounding box around the character faces, with their name as the tag.
- [ ] Locate and identify village symbols within each scene.
  - [ ] Determine the orientation of the found symbols and draw the corresponding box around them.
   - (Optional) If the headband symbol lays within a character bounding box, we can determine which village they are from.
   - (Optional) Detect if the village symbol on a headband has been crossed out (i.e. character is an ex-member of the village).
   - (Optional) Track characters with their respective headbands. 

### Notable Challenges
 - Some characters look really similar (e.g. Minato Namikaze, Naruto Uzumaki, Boruto Uzumaki)
 - Some characters wear their headbands in odd ways (e.g. Sakura Haruno)
 - Some characters largely change in appearance throughout the show