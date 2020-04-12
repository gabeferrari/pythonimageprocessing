import sys
import os
from PIL import Image

'''
#grab first and second argument with the image's paths
arguments in sys would be 
JPGtoPNGconverter.py [0]
Pokedex/ [1]
new/ [2]
which means that the terminal comand will be:
python3 JPGtoPNGconverter.py Pokedex/ New/
'''
image_folder = sys.argv[1]
output_folder = sys.argv[2]
'''
 check if the output folder exists
 if not it should be created
'''
if not os.path.exists(output_folder):
	os.makedirs(output_folder)
'''
loop through the folder
grab each image and convert them to the new folder
'''
for filename in os.listdir(image_folder):
	clean_name = os.path.splitext(filename)[0]
	img = Image.open(f'{image_folder}{filename}')
	img.save(f'{output_folder}/{clean_name}.png', 'png')
	print('Job done')
#print('Images converted and saved on new folder')
