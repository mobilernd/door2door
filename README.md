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

>> python manage.py runserver 8880

Congratulations , you already started your backend server    

## Front-End React
1- using your command line and go to folder path :

 C:\Users\MahmoudPasha\Desktop\frontend_react\ride-pooling 

Note that : in my PC machine i have the following path " 
{ your pc folder path }\ride-pooling 

So make sure your command line inside "ride-pooling" folder .

2- run this command :
>> npm install
3- npm start 

Untill this point your react server is started .

## How it works ? ( Back end and front end ) 
- Back end uses moc simulator , it creates `Simulator` instance (`Simulator(bounding_box)`) where `bounding_box` is a `tuple` that looks like this:
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

## Output Back end 
The `result` we get is a `dict` that looks like the following: 



![Untitled](https://user-images.githubusercontent.com/15266919/90051912-b66f1000-dcd8-11ea-98d6-b84871180da1.png)

