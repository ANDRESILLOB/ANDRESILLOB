# Using micropython on linux
IoThix developments using micro Python. Follow these instructions to set up the environment.

Please install virtualenv just once on PC, see: https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/

If you have problems with wheels see: https://pythonwheels.com/

1) Create a folder which will contain the project
2) Open it on VScode 
3) Create a virtual enviroment with this line on VScode workspace (folder) terminal
    ```
    python3 -m venv env	
    ```
4) Activate the virtual environment 
    ```
    source env/bin/activate
    ```
5) Install pip request
    ```
    pip3 install requests
    ```
6) Install ampy tool
    ```
    pip3 install adafruit-ampy
    ```
7) Deactivate de ESP debug (through serial terminal prompt - baudrate 115200) 
      ```
      import esp
      esp.osdebug(None)
      ```
8) Create the script with main.py name and run it on ESP
      ```
      ampy --port "here goes the port path" run main.py
      ```
9) Send the main.py file to ESP
      ```
      ampy --port "here goes the port path" put main.py
      ```
10) (optional) if you want to read files from the ESP
      ```
      ampy --port "here goes the port path" get "here goes the file name".py
      ```
11) when you finished the work of the day deactivate the virtual environment
      ```
      deactivate
      ```
For further work sessions just activate an deactivate the virtual environment

