### Setup debian linux for dummies

1) Download your prefered version of debian linux
2) Install linux
3) Update upgrade apt-get and apt
    ```
    sudo apt-get update
    sudo apt-get upgrade
    sudo apt update
    sudo apt upgrade
    ```
4) Install pip and setuptool for python3
    ```
    sudo apt-get install python3-pip
    sudo apt-get install python3-setuptools
    ```
5) Create alias for python inside of bashrc or profilerc
    ```
    alias python=python3
    ```
6) Add the user to dialout group
    ```
    sudo usermod -a -G dialout $USER
    ```
7) Reebot your pc
8) Again update upgrade apt-get and apt
9) Install git 
    ```
    sudo apt-get install git
    ```
    
### Enjoy your debian distro 
