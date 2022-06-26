## How to install OBS Plugins on MacOS

There are two ways to install OBS Plugins on MacOS.
We will be installing [OBS Virtual Background Plugin](https://obsproject.com/forum/resources/obs-virtual-background-plugin.1371/) in both examples. Download the zip file and extract it. Normally it should contain a `bin` and `data` folder.

Example for OBS Virtual Background Plugin:
![CleanShot 2022-06-26 at 14.43.07.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656243820684/SBVHt8Tqt.png align="left")

# First Method
This method is simpler but you may encounter issues when running the plugin.

Go to the folder `~/Library/Application Support/obs-studio`.  
If you navigate to it manually through Finder go to your user directory, right click and select `Show View Options` and then check the `Show Library Folder` checkbox as pictured below.
![CleanShot 2022-06-26 at 14.48.53.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656244190277/0zPd1evjK.png align="left")

Once you are in the `obs-studio` folder you will find a `plugins` folder. If you don't find it, create it yourself. After that copy the entire folder into `plugins` (in my case would be `obs-virtualbg` which contains both the `bin` and `data` folder).

![CleanShot 2022-06-26 at 15.02.01.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656244983939/r5RtKfnd6.png align="left")

Start OBS.

Now you might notice you get an error message as pictured below, if this happens try the second method and make sure to delete the folder you just copied from the `plugins` folder.

![CleanShot 2022-06-26 at 15.03.59.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656245189221/Fczx69qkV.png align="left")


# Second Method

Go to the `Applications` folder and find your .app file. Either `OBS.app` or another name for a modified version, I am using Stream Elements OBS so for me it is `SE.Live.app`. Right Click and select `Show Package Contents`, after that enter the `Contents` folder.

## Add the binary
In the folder of the extension, you have extracted previously, you will find a .so file in the `bin` folder. Copy that file to the `Plugins` folder. In my case I copy `obs-virtualbg.so` to the `Plugins` folder. If it asks you for a password or elevated permissions provide it so it can copy the file.

![CleanShot 2022-06-26 at 15.16.29.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656246727129/T7SgvANpy.png align="left")

## Add the data
To add the data we have to go to `Resources` -> `data` -> `obs-plugins`.  
In here create a folder with the same name as the .so file. I will create a folder with the name `obs-virtualbg` and copy inside it the contents of the `data` folder from the original plugin folder.

![CleanShot 2022-06-26 at 15.23.16.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656246222769/H4nfwPSbx.png align="left")

Now close the window and start OBS. You should find that obs started with no warning and the plugin runs as it should.

![CleanShot 2022-06-26 at 15.24.21@2x.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656246331704/Lm_vXh-k8.png align="left")
