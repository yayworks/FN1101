#!/bin/bash

export PYTHONPATH=/usr/local/anaconda3/envs/fenicsproject/lib:/usr/local/anaconda3/envs/fenicsproject/lib/python3.6:/usr/local/anaconda3/envs/fenicsproject/lib/python3.6/site-packages/:/usr/local/anaconda3/envs/fenicsproject/lib/python3.6/site-packages/matplotlib:$PYTHONPATH
source /usr/local/anaconda3/bin/activate fenicsproject

app_name="JupyterLab"
port=$1

token=`cat /dev/urandom | tr -dc 'a-z0-9' | fold -w 48 | head -n 1`

/usr/local/anaconda3/bin/jupyter lab --ip=0.0.0.0 --port=$port --LabApp.token=$token &

out_str=${app_name}:${port}/?token=${token}

echo ${out_str} >> /home/nimbix/.tokens.list
~                                                                                
