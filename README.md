# Introduction
This is my capstone project of my team and ITSC Company. This project aims to applicate computer vision in industrial robot. The hardware is providing by ITSC. We will code the software from computer vision unit, winform app and controller to control robot.
# Getting Started
Clone this repo
````bash
git clone
cd capstone_project_robot_grasping/
````
Create a environment, and install all required library, we used anaconda to create environment
````bash
conda create -n myenv python=3.10
conda activate myenv
pip install requirement.txt
````
running this command for using api endpoint
````bash
python my_cvu_api.py
````
Send the request with key-value pairs to the api endpoint
````bash
curl -X POST -H "Content-Type: multipart/form-data" \
			 -F "api_folder=<path/to/the/folder/which/api/will/run/in/this>" \
			 -F "output_folder=<relative/path/to/output/folder/you/want/to/save>" \
			 -F "img_path=<relative/path/to/the/image>" \
			 -F "template_path=<relative/path/to/the/template>" \
			 -F "threshold=0.75" \
			 -F "overlap=0.4" \
			 -F "method=cv2.TM_CCOEFF_NORMED" \
			 -F "min_modify=-1" \
			 -F "max_modify=1" \
			 -F "server_ip=<id address of your computer>"\
			 http://127.0.0.1:5000/my_cvu_api
````
Using Postman to send the request to api endpoint instead if you do not want to use command line.
# User Interface
Use Winform application to create UI.
