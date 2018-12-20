# HongBot

HongBOT Test

* ``heroku login``  
* Enter your credentials  
* ``git init``  
* ``heroku git:remote -a heroku_application_name`` Obviously replace heroku_application_name with the exact name you've given your heroku app when creating it  
* ``heroku buildpacks:set heroku/python``  
* ``heroku buildpacks:add https://github.com/Crazycatz00/heroku-buildpack-libopus.git``  
* ``heroku buildpacks:add https://github.com/jonathanong/heroku-buildpack-ffmpeg-latest.git``  
* ``heroku buildpacks:add https://github.com/guilherme-otran/heroku-buildpack-ffprobe.git``  
  
 **requirements.txt**  
```
git+https://github.com/Rapptz/discord.py@rewrite#egg=discord.py[voice]
pip
youtube_dl==2018.11.07
colorlog
cffi --only-binary all; 
aiohttp ~= 2.3.10
websockets
chardet
opuslib
pynacl==1.2.1
```

**runtime.txt**  
```
python-3.7.0
```

 **Procfile** (no extension)  
```
worker: python run.py
```

