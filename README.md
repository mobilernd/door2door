# What should you do to run this project ?

Please follow up the following steps in arrangement  ( please start with backend first ) .

# BackEnd-Django

Do the following steps to run your BackEnd-Django .

1- Using Any Editor ( i'm using VS Code Editor ) go to your project folder below ( that is apprear in my machine and you will get another one .

C:\Users\MahmoudPasha\Desktop\mobility-app\Django-simulator

Please use your current porject folder path and the last path name is "Django-simulator" , it will be like this : 

{ your project path here }\Django-simulator 

2- Do not forget to activate virtual environment , you are now in folder name "Django-simulator" , you will find a folder inside it called "Scripts" , 
In your command line write the following : 
>> ./Scripts/activate 

3- Make sure that you have installed all back end libs in file name requirments.txt , write the following command : 

>> pip install requirements.txt


4- Now we want to call and run file called "manage.py" to run python server , this file ( manage.py) is inside folder name "project" , go to this folder first 
>> cd project 

then write the following command to start python server ( please use port number 8880 because i used this port in front end ( react ) ) 

>> python manage.py runserver

Congratulations , you already started your backend server    

## Setup
1. Initialize a virtual environment and install the requirements in `requirements.txt`.
2. Adjust `Simulator.path_to_stops` based on the final architecture of the project/where it will be run from.

## Usage
- Create a `Simulator` instance (`Simulator(bounding_box)`) where `bounding_box` is a `tuple` that looks like this:
```python
# bounding_box = (min_longitude, min_latitude, max_longitude, max_latitude)
bounding_box = (13.34014892578125, 52.52791908000258, 13.506317138671875, 52.562995039558004)
```
The bounding box has to be in Berlin.

- Get the simulation results:
```python
result = Simulator(bounding_box).simulate(number_of_requests)
```
where `number_of_requests` is the number of requests to our Ridepooling service to "simulate".

## Output
The `result` we get is a `dict` that looks like the following:

| Key                           | Type                                                               | Description                                                                                                                     |
|-------------------------------|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `booking_distance_bins`       | dict                                                               | How many bookings happened for every "kilometer bin". E.g. how many bookings had a distance between 0 and 1km, 1 and 2kms, etc. |
| `most_popular_dropoff_points` | String (valid [`.geojson`](https://en.wikipedia.org/wiki/GeoJSON)) | Which points within the simulated bounding box were the most popular dropoff points.                                            |
| `most_popular_pickup_points`  | String (valid [`.geojson`](https://en.wikipedia.org/wiki/GeoJSON)) | Which points within the simulated bounding box were the most popular pickup points.                                             |
