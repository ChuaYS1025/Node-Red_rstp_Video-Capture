# Node-Red_rstp_Video-Capture
Using rstp protocol with node-red to capture video from an IP/POE camera

Capture video(s) using node-red on specific time or condition 

Items/software to install:

Install ffmpeg >> sudo apt install -y ffmpeg

Under Node-Red:

**In node-red exec node**

"ffmpeg -i rtsp://admin:password@192.168.1.41:554/ch01.264 -s 640x480 -b:v 1000k -r 8 -t 30 -y -vcodec copy -an"

rtsp://admin:password@192.168.1.41:554 >> username, password, IP address of the camera

ch01.264 >> camera using h264 

-s 640x480 >> resolution of the video

-b:v 1000K >> Constant Bit Rate (CBR) mode

-r >> frame rate per seconds

-t >> timer

-vcodec >> video decoder

-an >> save file location 

![image](https://github.com/ChuaYS1025/Node-Red_rstp_Video-Capture/assets/106689692/ba327d1b-e2b5-48e9-814e-62f86275cda8)

Suggestions for improvement:

Can integrate with other node or functions to make it to your own applications. 

Credit to https://flows.nodered.org/flow/0da4d606575df13700461400178aca4e 
