# Data Science 1
Tuesday, January 30th 2024

### Configuring your Device for Data Science 1

**AIM:** What tasks must we complete to configure our devices for Data Science 1?

**OUTCOME ALIGNMENT:**

<ins>IEC.TYS65T.6</ins>: Model employability skills such as personal mindset, planning for success, and collaboration.

**SUCCESS CRITERIA:**
- [ ] I have created a new repo on GitHub named `Computer_Science_Portfolio`.
- [ ] I have shared my `Computer_Science_Portfolio` repo with Mr. Swotinsky.
- [ ] I have installed Git on my virtual machine.
- [ ] I have cloned my `Computer_Science_Portfolio` repo to my virtual machine.
- [ ] I have created a subdirectory named `Data_Science_1` within my `Computer_Science_Portfolio` repo on my virtual machine.
- [ ] I have installed Anaconda Navigator and Jupyter Notebook on my virtual machine.
- [ ] I have added Jupyter's installation path to my virtual machine's path environment variable.
- [ ] I have created a batch file on the desktop of my virtual machine that launches Jupyter Notebook from `Data_Science_1`.
- [ ] I have added, committed, and pushed `movie_genre_data.ipynb` to GitHub.


**DO NOW:** Write down your favorite movie genre...Action, Comedy, or Horror?

**AGENDA:**

1. Movie Genre Survey
2. Syllabus Review
3. Configuration Tasks (see reference section below.)

**HOMEWORK:** No homework, but if you have not successfully completed all configuration tasks by the end of class, you must see Mr. Swotinsky at the end of the day for support.

##
**REFERENCE:**

## Configuration Task 1: Download Jupyter to your virtual machine (using Anaconda Navigator).

1. Open a web browser and navigate to https://anaconda.com/download.
2. Click <ins>Download</ins>.
3. Run the installer.

**Installation may take a while.  While Anaconda installs, you may work on Configuration Task 2.  However, you must complete all parts of Configuration Tasks 1 and 2 before you proceed to Configuration Task 3.**

4. After installation is complete, navigate to the your virtual machine's desktop.
5. Search for and right-click `Jupyter Notebook`.
6. Select <ins>Pin to taskbar</ins>.

## Configuration Task 2: Create, Share, and Clone a New Repo on GitHub.
*When you are ready to show off your work, this repo will serve as your public-facing Computer Science Portfolio.*

**PART A:** Download Git to your virtual machine:

1. Open a web browser and navigate to https://git-scm.com/downloads
2. Click the top link to download the latest version of Git for Windows.
3. Run the installer.
4. On the <ins>Select components</ins> screen, select <ins>Additional Items</ins>, and <ins>On the Desktop</ins>.  Do not make any other changes.


**PART B:** Create a new repo:  

1. Navigate to your GitHub profile (github.com/YourUserName)
2. Click <ins>Repositories</ins>.
3. Click <ins>New</ins>.
4. Name your repository, **Computer_Science_Portfolio**.
5. For now, your repository does not need a description.
6. Set your repository to **Private**.  
7. Select **Add a README file**.
8. Leave the .gitignore template set to **None**.
9. Select a **Creative Commons Zero v1.0 Universal** license.
10. Click <ins> Create repository</ins>.

**PART C:** Share your repo:

1. Click <ins>Settings</ins>.
2. Click <ins>Collaborators</ins>. (You may be prompted to sign in to GitHub again.)
3. Click <ins>Add people</ins>.
4. Add jswotinsky@schools.nyc.gov.

**PART D:** Clone your repo:

*During this process, you may be prompted to sign in to GitHub again.*
1. Launch Git Bash using the icon on the desktop of your virtual machine. 
2. Change the directory to your Python312 folder by entering the command below:
```
cd AppData/Local/Programs/Python/Python312
```
3. Clone your repo by entering the command below: 

**Note: In the command below you must change `YourGitHubUserName` to your actual GitHub username.**

```
git clone https://github.com/YourGitHubUserName/Computer_Science_Portfolio.git
```
4. Change the directory to your newly cloned Computer Science Portfolio repo by entering the command below:

```
cd Computer_Science_Portfolio
```
5. Create a sub-directory for Data Science 1 by entering the command below:
```
mkdir Data_Science_1
```

## Configuration Task 3: Add Jupyter's installation path to your virtual machine's path environment variable.

**STOP:** Have you completed all parts of Configuration Task 1 and 2?   
**If not, go back to complete Configuration Tasks 1 and 2 before proceeding to Configuration Task 3.**


**PART A:** Identify and copy Jupyter's installation path:
	
1. Navigate to the your virtual machine's desktop.
2. Search for and right-click `jupyter.exe`.
3. Select <ins>Open file location</ins>.
4. Copy Jupyter's installation path from the address bar.
<br>**Note:** Jupyter's installation path should be `C:\Users\FirstInitialLastName\anaconda3\Scripts`.

**PART B:** Add Jupyter's installation path to your virtual machine's path environment variable:

1. Navigate to your virtual machine's system properties:
<br>(<ins>Windows Icon</ins> > <ins>Settings</ins> > <ins>System</ins> > <ins>About</ins> > <ins>Advanced System Settings</ins>).
  
2. Select the <ins>Advanced</ins> tab.
3. Click <ins>Environment Variables</ins>.
4. Highlight the <ins>Path</ins> row.
5. Click <ins>Edit</ins>.
6. Click <ins>New</ins>.
7. Paste the path you copied in STEP 1.
8. Click <ins>OK</ins>.

		
## Configuration Task 4: Write a small batch file to launch Jupyter Notebook from your Data Science 1 repo directory.

**STOP:** Have you completed all parts of Configuration Tasks 1, 2, and 3?   
**If not, go back to complete Configuration Tasks 1, 2, and 3 before proceeding to Configuration Task 4.**

**PART A:** Write your batch file:
1. Open Notepad.
2. Copy/Paste the code below to your file:
```
cd..

cd AppData\Local\Programs\Python\Python312\Computer_Science_Portfolio\Data_Science_1

jupyter notebook
```

**PART B:** Save your batch file:
1. For <ins>Save as type</ins>, select <ins>All Files</ins>.
2. For <ins>Encoding</ins>, select <ins>ANSI</ins>.
3. Name your file `jupyter_launcher.bat`.
4. Save `jupyter_launcher.bat` to your virtual machine's desktop.


## Configuration Task 5: Test your configuration.

**STOP:** Have you completed all parts of Configuration Tasks 1, 2, 3, and 4?   
**If not, go back to complete Configuration Tasks 1, 2, 3, and 4 before proceeding to Configuration Task 5.**

**PART A:** Create your first Jupyter Notebook:

1. Use the jupyter launcher you created in configuration task 4 to launch Jupyter.
2. Click <ins>New</ins>.
3. Select <ins>Python 3 (ipykernel)</ins>.
4. Rename your notebook, **movie_genre_data**.
5. Copy/Paste the code below to the first cell of your notebook:

```python
import matplotlib.pyplot as plt
import numpy as np

action_count = 1
comedy_count = 1
horror_count = 1

var = np.array([action_count, comedy_count, horror_count])
genres = ['Action','Comedy','Horror']

plt.pie(var, labels = genres)
plt.title('Favorite Movie Genres')

plt.show()
```

6. Click <ins>Run</ins>.
7. <ins>Save</ins> your file.

**PART B:** Push your notebook to your repo:

1. Launch Git Bash. 
2. Navigate to the Data Science 1 subdirectory of your Computer Science Portfolio repo by entering the command below:

```
cd AppData/Local/Programs/Python/Python312/Computer_Science_Portfolio/Data_Science_1
```

3. Track your `movie_genre_data.ipynb` file by entering the command below:

```
git add movie_genre_data.ipynb
```

4. Commit your changes to `movie_genre_data.ipynb` file (including the message: 'Uploaded v0 of movie_genre_data.')by entering the command below :

```
git commit movie_genre_data.ipynb -m 'Uploaded v0 of movie_genre_data.ipynb'
```

5. Push your repo to GitHub by entering the command below :

```
git push
```
6. Navigate to your Computer Science Portfolio on GitHub to confirm that the `Data_Science_1` subdirectory and `movie_genre_data.ipynb` notebook you pushed are visible.

### Congratulations! Your device is now configured for Data Science 1!

## If you run into any challenges, remember to troubleshoot by...
* ...reviewing the directions above.
* ...consulting with colleagues.
* ...asking for help.
* ...consulting web-based resources.
* ...etc.
