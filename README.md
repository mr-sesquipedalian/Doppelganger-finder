# Bollywood Celebrity Doppleganger Finder

## To Run The Code:
The first time you run the code, uncompress `train_dir.zip` and `clf.joblib.zip`.

Run the following commands:
```
virtualenv --system-site-packages -p python3 ./venv
source ./venv/bin/activate  # sh, bash, ksh, or zsh
find . -name "*.DS_Store" -type f -delete
python svm.py
```
## Useful Bash Scripts:
For the [Indian Movie Dataset](http://cvit.iiit.ac.in/projects/IMFDB/):

```
for d in ./*/ ;
do
        cd "$d" || exit; # enter each dir if it exists
				find . -mindepth 2 -type f -print -exec mv {} . \;  # merge all files 2 levels deep
        find . -type f ! -name '*.jpg' -exec rm '{}' +  # find and rm any non jpg
        ls -d  */ | xargs rm -rf;  # delete any empty dirs
        cd ..; # back to parent dir
done
```

