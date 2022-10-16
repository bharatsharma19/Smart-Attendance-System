# attendance-management-system
[![Python 3.6](https://img.shields.io/badge/python-3.6-blue.svg)](https://www.python.org/downloads/release/python-360/)  
A Face Recognition-based project in Python to mark and track your attendance.

### System/Code Requirements
- Python 3.6 or above
- Roboto Font (`pip install font-roboto`)
- OpenCV (`pip install opencv-python`)
- Tkinter (Available in Python)
- PIL (`pip install Pillow`)
- Pandas (`pip install pandas`)
- OpenCV contrib (`pip install opencv-contrib-python`)
- PyMySQL (`pip install pymysql`)
- WampServer (for database)
- Anaconda (preferred)

### Steps to Run
- Download the Repository as a `.zip` file (`attendance-management-system.zip`)
- Extract the contents of the .zip file into the folder attendace-management-system (if this folder is not created automatically, then create a new folder first and then extract the .zip file into it)
- Create a new `TrainingImage` folder in that folder
- Open file `AMS_Run.py` with a code editor (like `VS Code`) and change all the paths with your corresponding system paths (line nos. 168, 224, 485, 514, 554)
- Run file `AMS_Run.py` (in Command Prompt/Anaconda Prompt/ any Terminal, open the folder attendance-management-system and run cmd: `python AMS_Run.py`)


### Project Structure

- After you run the cmd, the FAMS - Face Recognition Based Attendance Management System application opens in a new window
- For every new student you need to give his/her face data to the system. So enter his/her Roll No. and Name then click on `Take Images` button
- It will collect 200 images of his/her face, and saves those images in the `TrainingImage` folder
- After that we need to train the model, so click on `Train Images` button
- Model (`Trainer.yml`) is saved in `TrainingImageLabel` folder
- It will take 5-10 mins for training (for 10 person data) (so about 1 min for 1 person data)
- After training is completed, either click on `Automatic Attendance` or `Manually Fill Attendance` button
- `Automatic Attendance` will fill the attendance automatically from your face (by Face Recognition) using the trained model
- It will create `.csv` file of attendance according to Time & Subject
- You can also store this data in your own database (install WampServer), and change the DB name accordingly in the code in file `AMS_Run.py`
- `Manually Fill Attendance` is to fill the attendance of a student manually (without Face Recognition)
- It will also create a `.csv` file of attendance and store in a database
- To see the details of all the registered students, click on `Check Registered Students` button
- It will open the Admin Login Panel, enter the correct username and password (mentioned in code) and `StudentDetails.csv` file opens