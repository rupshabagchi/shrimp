# Shroominen

An app that helps you pick edible Finnish mushrooms!

## Table of Contents
* [Goal](#goal)
* [Issues ran into](#issues)
* [General guidance on mushroom classification](#guidance)
* [Data](#data)
* [Data Models](#models)

## <a name="goal"/> Goal of the app

The goal is to classify pictures of common mushrooms with a web application.

## <a name="issues"/> Issues
The main issue is getting good quality data for the training and then removing images which have issues such as bad lighting, angle, blurriness or background noise.

## <a name="guidance"/> General guidance on mushroom classification (from images)

* Note where the mushroom grows: is it on the ground or on wood?

 If it grows on ground it could be a saprotroph of detritus (karikkeen lahottaja), mycorrhiza (juurisieni) which is specific type of mushroom living from the roots of a tree or it could still be a saprotroph of a tree but the wood is on ground level.  
 If it grows on wood consider if it's conifer(havupuu) or hardwood(lehtipuu). Some species grow on only a very specific wood like oak.  
 
* Do not consider the time of year to be a indicator of any sort. Every year the seasons length differ so one year the mushroom season might start way later than the next year.  
* Underneath the mushroom cap can be different types of gills in various combinations. (TODO)  
* Surface of the cap is also a very good classifier of the mushroom. The structure might not be possible to know from a picture though.  
* Color of the mushroom varies a lot depending on the humidity and the age of the mushroom. When raining the colors get deeper and more distinctive. Young mushrooms have stronger colors than old ones. Also sunlight might diminish the colors.  
* Stem(jalka) of a mushroom can also indicate a lot of information from the mushroom. Thin and thick shapes are more distinctive than average size.  
* Geographic location of the mushroom could be useful as some species probably don't grow everywhere in Finland.

There is also a lot of data such as smell and touch that could be used but then user would have to input it themselves.


## <a name="data"/> Data  

### <a name="sources"/> Sources

* [Mushroom World](http://www.mushroom.world)
* [Lajit](http://tun.fi/HBF.25786?locale=en)
* [Luontoportti](http://www.luontoportti.com/suomi/fi/sienet/)
* [Funga](http://www.funga.fi/teema-aiheet/sienten-tunnistaminen/)

### <a name="import"/> Downloading and importing the dataset

The data was scraped from from mushroom.world website using a scraper beforehand. The images and the metadata are stored in both Google Drive and Amazon S3. But since Google Drive doesn't support direct downloads (like wtf) I had to put the file in S3 too. With public access rights, yay.

The pictures are `.jpg` pictures resized to a standard 480x480 size. (Or 360x480?)

### <a name="model"/> Models:

#### Mushroom Class 

| Data       | Meaning         | 
| ------------- |:-------------:| 
| name_fin     | Finnish name| 
| name_eng   | English name| 
| name_latin  | Latin name| 
| url_mw  | URL for Mushroom-world |
| url_wiki?  | URL for Wikipedia |
| url_lajit?  | URL for Lajit.fi |
| edibility  | edible/poisonous/inedible |


### Mushroom Images

| Data       | Meaning         | 
| ------------- |:-------------:| 
| name_latin  | Latin name| 
| name_img  | Name of the image file |
| img_url  | URL to the original picture |
| file_path  | Image Path | 
