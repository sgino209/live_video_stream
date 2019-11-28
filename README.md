# Live Video Stream (Flask+OpenCV)    
    
WebStreaming + Motion detector algorithm will detect motion by form of background subtraction    
    
## Prerequisites:    
- pip install flask    
- pip install numpy    
- pip install opencv-contrib-python    
- pip install imutils    
    
## Usage Examples:    
Live streaming from local device, i.e. camera which is physically connected to the host machine/server (both commands are equivalent):    
*% python app.py --device_ip 0.0.0.0 --server_port 8000*    
*% env DEVICE_IP="0.0.0.0" SERVER_PORT=8000 ./app.py*    

Live streaming from Spain:    
*% env DEVICE_IP="0.0.0.0" SERVER_PORT=8000 REMOTE_IP="http://109.186.51.37:60001/cgi-bin/snapshot.cgi?chn=0&u=admin&p=&q=0&COUNTER" ./app.py*    
    
Live streaming from Israel:    
*% env DEVICE_IP="0.0.0.0" SERVER_PORT=8000 REMOTE_IP="http://185.10.80.33:8082/cgi-bin/faststream.jpg?stream=half&fps=15&rand=COUNTER" ./app.py*    
    
## Note:    
MULTI_THREAD_EN env can be applied for enabling/disabling multi-thread setup, i.e. whether or not video processing    
will be done in a separate thread or not (might become sensitive when running in a production server).    
    
## References:    
1. https://www.pyimagesearch.com/2019/09/02/opencv-stream-video-to-web-browser-html-page    
2. https://www.pyimagesearch.com/2019/04/15/live-video-streaming-over-network-with-opencv-and-imagezmq    
3. https://www.pyimagesearch.com/2017/02/06/faster-video-file-fps-with-cv2-videocapture-and-opencv    
4. https://stackabuse.com/deploying-a-flask-application-to-heroku    
5. https://github.com/mrxmamun/camera-live-streaming    
6. https://github.com/mrxmamun/live-stream-face-detection    
6. https://www.insecam.org    
