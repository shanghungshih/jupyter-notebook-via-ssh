# jupyter-notebook-via-ssh

- download [Anaconda](https://www.anaconda.com/download/#linux)
    - `wget https://repo.anaconda.com/archive/Anaconda3-5.3.1-Linux-x86_64.sh .`

- run on server (ex. testuser@140.112.999.999)
    - recommand to run with screen `screen -S jupyter`
        - `screen -S <screen_name>`: start a new screen
        - `screen -ls`: check out current screen list (ex. 12345.jupyter)
        - `screen -r 12` or `screen -r jupyter`: attach to 12345.jupyter
        - to detach a screen: `ctrl+A+D` in screen
        - to shutdown a screen: `ctrl+D` in screen
    - `jupyter notebook --generate-config`: generate jupyter configure file
    - `jupyter notebook password`: setup your password instead of token
    - `jupyter notebook --no-browser --port=8888`: activate jupyter notebook
    
- connect from local host 
    - `ssh -N -f -L localhost:8889:localhost:8888 testuser@140.112.999.999`: connect via ssh
    - http://localhost:8889/
