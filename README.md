# termux-scipt-for-XVoard
a script to run in termux to get XVoard apk
# Requirements
- <a href="https://f-droid.org/en/packages/com.termux/">Termux App</a>
- <a href="https://github.com/ANTI-XV/XVoard">XVoard source code</a>
- at least 800mb storage
# installation 
1. Download the XVoard source code from the link above
2. open termux and run this script:

```pkg update && pkg upgrade -y && termux-setup-storage && pkg install -y unzip && pkg install -y which && pkg install -y aapt2 && pkg install -y openjdk-21 git wget && wget https://raw.githubusercontent.com/iBotPeaches/Apktool/master/scripts/linux/apktool && chmod +x apktool && wget https://github.com/iBotPeaches/Apktool/releases/download/v3.0.2/apktool_3.0.2.jar -O apktool.jar && mv apktool "$PREFIX/bin/" && mv apktool.jar "$PREFIX/bin/" && cd /sdcard/Download && unzip XVoard-main.zip && cd /sdcard/Download/XVoard-main && apktool b . --aapt $(which aapt2) && cd .. && wget -q https://github.com/patrickfav/uber-apk-signer/releases/download/v1.3.0/uber-apk-signer-1.3.0.jar -O uber-apk-signer.jar && mv uber-apk-signer.jar ~/ && cd && java -jar uber-apk-signer.jar --apks /sdcard/Download/XVoard-main/dist/XVoard_FPC.apk```

3. open your file manager and go to /sdcard/Download/XVoard-main/dist you will find aan apk called XVoard-v3-FAC_mod-aligned-debugSigned.apk ( or something similar )
4. install XVoard-v3-FAC_mod-aligned-debugSigned.apk
and you are done
# IMPORTANT NOTE'S
1. the script will take at least 6 minutes depending on your internet speed
2. in the mid of that script termux will ask you for all file's access , Grant that , it is needed to locate where the XVoard-main.zip is and do the work with it
3. while the script is running it will ask you for somethings to you accept that some downloaded things will take storage , if it says at the end [y/N] type y and hit enter , if it says other things type N
