# Shroominen

An app that helps you pick edible Finnish mushrooms!

## Goal

The goal is to classify pictures of (common) mushrooms with a web application.

Challenge is to get good quality data for the training and then negate some common problems with images such as: lighting, angle, blurriness and background noise.

Current plan is to classify only the poisonous mushrooms of Finland along with some common edible and un-edible ones. Probably using Convolutional Neural Network.


### Preliminary Models:

#### Mushroom Class
* name_fin - Finnish name
* name_eng - English name
* name_latin - Latin name
* url_mw - Mushroom-world url
* url_wiki? - Wikipedia url
* url_lajit? - Lajit.fi url
* img_urls? - List of links to its images. Probably should be deleted.
* edibility - edible/poisonous/inedible

### Mushroom Image
* name_latin - Latin name
* name_img - Name of the image file
* img_url - URL to the original picture
* file_path - Path to the image from the root of its containing folder.
