This is modified from:
   https://github.com/crjens/PiPowerMeter
   
   - only one voltage channel - single phase;
   - only load channel, no source or both;
   - board number is reduced to 7 instead of 8;
   - removed board decoder - BS is from Pi pin;
   -...
   
   Software Installation
---------------------
1. Any of the full size Raspberry Pi models with the 40 pin header are supported including: V1 A+, V1 B+, V2, V3 B, V3 B+ and V4 B.  The additional memory and computing power of the V2/V3/V4 models is recommended.
2. Start with latest Raspbian image from http://downloads.raspberrypi.org/raspbian_lite_latest
	1. (verified with Raspbian Buster 2020-02-13)
	2. It's recommended that you use the Lite version because it's smaller and installs faster but you can use either.
3. login to Pi with Putty or other ssh client
	1. the latest versions of Raspbian have ssh disabled.  You can enable ssh via raspi-config or just create an empty file named 'ssh' in the boot partition of the sd card.
4. Install the PiPowerMeter software by running the following command (you must install with root privileges such as the built-in pi account):
	1. wget -O - https://raw.githubusercontent.com/i144/myPowerMeter/master/setup.sh | bash
5. run 'sudo raspi-config' 
	1. set locale and timezone under Localisation options
	2. expand filesystem under Advanced options
	3. change user password (optional)
	4. reboot when prompted after exiting raspi-config
6. Open your browser to http://<Your Raspberry Pi's IP Address>:3000
