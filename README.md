# OTA_APK_Extractor
This script utilises [payload dumper](https://github.com/vm03/payload_dumper) and [image extractor](https://ihax.io/mtk-extractor/) tools to extract the apps from the system.img of an android OTA file. It works on Windows OS.

## Requirements:
- Windows 10
- Python3 installed and added to environment variable
- pip3 installed and added to environment variable
- Python Modules -> protobuf==3.6.0, six==1.11.0, bsdiff4>=1.1.5
- If you face issues, install Windows 10 SDK & C++ build tools. Download the build tools [here](https://visualstudio.microsoft.com/visual-cpp-build-tools/). Launch the Visual Studio Installer and select the Desktop development with C++ option. Install the default tool options for this. Upgrade the setuptools using the command **python -m pip install --upgrade setuptools** 

Install the python modules using the requirements file:
**python -m pip install -r requirements.txt --user**

## Extractor script usage:
1. Extract the OTA file.
2. Copy the full path of the payload.bin file present in the extracted OTA file, e.g. C:\root\ota 1\payload.bin
3. Run the script - **python Extractor.py**
4. When prompted enter the full path of the payload.bin
5. The system.img will get extrcated from payload.bin 
6. You will be presented 2 options - you can either extract all apps or you can extract specific apps that you want to extract.
7. To extract all apps choose option **1**
     ![User_Choice_1](https://user-images.githubusercontent.com/49153415/148209249-28612539-34cb-4f6c-a35b-b90a62bda505.png)

8. To extract specific apps, choose option **2**
9. It will display the total number of apps on the image.
10. Enter the number of apps that you want to extract.
11. Enter the names of the apps that you want to extract. You have to enter full name of the APK e.g. <br/>
    CertInstaller.apk <br/>
    BasicDreams.apk <br/>
    KeyChain.apk <br/>

    ![User_Choice_2](https://user-images.githubusercontent.com/49153415/148209266-3bd739cc-9028-4c58-9110-a200a601dcbc.png)

12. The extracted apps will be present in the output folder.

