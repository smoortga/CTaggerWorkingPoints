# CTaggerWorkingPoints
This repository serves to automatize the CMS c-tagging working point calculation

### Step 1: setup the repo
login to lxplus7 and do
```
cmsrel CMSSW_10_6_12
cd CMSSW_10_6_12/src
cmsenv
git clone https://github.com/smoortga/CTaggerWorkingPoints.git
cd CTaggerWorkingPoints
mkdir plots
```

### Step 2: connect to the notebook
Connect to lxplus7 and navigate to the CTaggerWorkingPoints directory. Then do:
```
jupyter notebook --no-browser --port=4444
```
A message will appear that provides you with a link that you can copy to your local webbrowser later on.

Meanwhile, open another tab and do the following to create an ssh port:
```
ssh -N -L localhost:4444:localhost:4444 login@lxplusxxx.cern.ch 
```
with XXX corresponding to the lxplus machine to which you are logged in in the first tab.

Then you can just copy-paste the provided link of your first command in your brower and it should open up the jupyter notebook interface. You can then connect to the [ctagger_workingpoint_derivation.ipynb](./ctagger_workingpoint_derivation.ipynb) notebook and run it.
