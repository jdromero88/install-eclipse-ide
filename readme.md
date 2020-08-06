# Install Eclipse IDE and say HELLO WORLD from Java
## Step 1
Download [Eclipse-IDE](https://www.eclipse.org/downloads/)
![Download Eclipse](/img/download-eclipse.gif)

## Step 2
Create a folder where we want to install Eclipse. I'm going to name it eclipse-ide-2020‑06 but you can name it whatever you want.
To do this we need to open a Terminal you can do it pressing Ctrl + Alt + t
and type:
```
mkdir /home/your-user/eclipse-ide-2020‑06
```
*make sure you replace 'your-user' with your username.*
![Create Eclipse directory](/img/create-eclipse-folder.gif)

## Step 3
We need to extract eclipse into the directory we created:
In your terminal type:
```
tar -zxvf /home/your-user/Downloads/eclipse-inst-linux64.tar.gz -C /home/your-user/eclipse-ide-2020-06/
```
*make sure your paths are correct.*
*make sure you replace 'your-user' with your username.*
![extract Eclipse](/img/extract-eclipse.gif)

## Step 4
Now finally is time to install it. To run the installer type in your terminal:
```
sudo /home/your-user/eclipse-ide-2020-06/eclipse-installer/eclipse-inst
```
is going to ask you for your password.
*make sure you replace 'your-user' with your username.*
![run Eclipse installer](/img/run-eclipse-installer.gif)

## Step 5
Click on the option you want to install in this case click on Eclipse IDE for Java Developer and pick the directory you want to install in my case I want to install it on this directory
![directory to install](/img/directory-to-install.png)

*So I'm going to change root for opt*
![installing eclipse ide for java developers](/img/installing-eclipse-ide-java-developer.gif)
*Accept the license and Ooomph. When is done installing just click on launch*

## Step 6
Click on the option you want to install in this case click on Eclipse IDE for Java Developer and pick the directory you want to install in my case I want to install it on this directory
![directory to install](/img/directory-to-install.png)

*So I'm going to change root for opt*
![installing eclipse ide for java developers](/img/installing-eclipse-ide-java-developer.gif)
*During the installation maybe is going to ask you to accept unisgned content for Ooomph just click accept*

## Step 7
After launch it is going to ask you to create a workspace (A workspace is where Eclipse is going to keep all the eclipse projects by default)
![Eclipse workspace](/img/create-workspace.gif)
![Eclipse workspace 2](/img/create-workspace-2.gif)
![Eclipse IDE in Linux Mint](/img/eclipse-for-linux-mint.gif)

## Step 8

To create a desktop icon run the next command in your terminal:
```
sudo xed .local/share/applications/eclipse.desktop
```

is going to open a text editor and paste this inside and save it.
```
[Desktop Entry]
Encoding=UTF-8
Name=Eclipse IDE
Comment=Eclipse Integrated Development Environment
Exec=/opt/eclipse/java-2020-06/eclipse/eclipse
Icon=/opt/eclipse/java-2020-06/eclipse/icon.xpm
Categories=Application;Development;Java;IDE
Version=1.0
Type=Application
```

To use the new launcher outside the dash we need to change the permission:
```
sudo chmod +x ~/.local/share/applications/eclipse.desktop
```
![Create Eclipse icon](/img/create-desktop-icon.gif)

## Step 9

Now is time to open the folder where is the launcher.
```
xdg-open .local/share/applications/
```
![Create Eclipse icon](/img/open-launcher-folder.gif)
*you may have this problem 'the eclipse executable launcher was unable to locate its companion shared library'*
To fix this run:
```
sudo chmod 775 -R /root/
```
and then just execute again the launcher. Then you can find the launcher under Menu > Programming
![Fix shared library](/img/fix-shared-library.gif)

![New Launcher](/img/new-launcher.gif)
-----
# Create Hello World app
