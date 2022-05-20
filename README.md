# VoxCeleb2-Dataset
This repository goes over steps to download and extracting VoxCeleb2 dataset.



```
// To download full voxceleb2 dataset.
python3 ./dataprep.py --save_path /path/to/dir --download --user voxceleb1912 --password 0s42xuw6

// To download partial/test voxceleb2 dataset.
python3 ./dataprep.py --save_path /path/to/dir --download --user voxceleb1912 --password 0s42xuw6 --test_dataset
```


```
cd YOUR_DIR_PATH  //Move to the folder where you downloaded the dataset.

//To concatenate the files downloaded
cat vox2_dev_mp4 * > vox2_mp4.zip
```

```
unzip vox2_mp4.zip -d /path/to/dir
```

Extra commands to double check the number of sample downloaded 
```
//Count number of folder in dir
ls -l | grep -c ^d 

//Sum number of item in folder, in dir
ls -l | awk '{sum+=$2} END {print sum}'

//Sum number of file in dir, recursively
find DIRNAME -type f | wc -l	//outside dir
find -type f | wc -l			//from within 			
```
NOTE: "^d" : is a caret, and it mean grep only a line that start with "d"


