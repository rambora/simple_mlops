create a new conda environment : conda create -n wineq python=3.7 -y
activate the new environment : conda activate wineq
create a 'requirements.txt' file
pip install -r requirements.txt
create template.py file
python template.py
git init
dvc init
dvc add data_given/winequality.csv
git add .
git commit -m "first commit"
git add . && git commit -m "update Readme.md"
git remote add origin https://github.com/rambora/simple_mlops.git
git branch -M main
git push -u origin main
create params.yaml and dvc.yaml
touch src/get_data.py
write the get_data.py
touch src/load_data.py 
write the load_data.py - writes 'winequality.csv' to "src/raw"
run "dvc repro" - runs the stages in the "dvc.yaml" file- this creates a "dvc.lock" file
touch src/split_data.py
run "dvc repro" - this creates a "dvc.lock" file