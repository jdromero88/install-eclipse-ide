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
After launch it is going to ask you to create a workspace (A workspace is where Eclipse is going to keep all the eclipse projects by default)
![Eclipse workspace](/img/create-workspace.gif)
![Eclipse workspace 2](/img/create-workspace-2.gif)
![Eclipse IDE in Linux Mint](/img/eclipse-for-linux-mint.gif)

## Step 7

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

## Step 8

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
____________
# Create Hello World app with text editor
To do this just create a new directory you can name whatever you want and inside create a file hello-world.java and just paste this:
```
// Create the class HelloWorld
class HelloWorld{
  // Call the main() method to start our application
  public static void main(String args[]){
    // Print Hello World in terminal
    System.out.println("Hola Mundo desde Java!");
    System.out.println("Hello World form Java!");
  }
}
```

Now we need to compile our application to do this in your terminal type:
```
javac hello-world.java
```

This would create a new file called HelloWorld.class and now we need to run our app. In the terminal run:
```
java HelloWorld
```

and that is! you should see Hola Mundo desde Java! and Hello World from Java! in your terminal. Congrats! This is your first java app!

____________
# Create Hello World app with Eclipse IDE
Open Eclipse IDE go to Menu > Programming > Eclipse IDE

Then we need to create a new java project. Click in File > New > Java Project and give it a name hello-world and click finish.
![Create new project](/img/create-hello-world-app.gif)

Now we need to create a package inside the folder src. Put your cursor inside the Package Explorer and right click > New > Package > give it a name and click finish.
![Create print package](/img/create-print-package.gif)

Time to create the HelloWorld class. Again go to Package Explorer and right click > New > Class name it HelloWorld. > Tick public static void main(String[] args). Click finish.
![Create HelloWorld class](/img/create-helloworld-class.gif)

After created the class, the IDE will generate already some base code and would look like this:
```
package print;

public class HelloWorld {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

	}

}
```

You already know how to print string in the terminal. Go ahead and type the code inside the main method. In case you don't remember here it is.
```
System.out.println("Hello World form Java!");
```
![Print HelloWorld](/img/print-hello-world.gif)

Now is time to run the app. To do this just click on the play icon or go to the menu Run > Run. Now you should see Hello World from Java in the IDE terminal.
![Run the project](/img/run-the-project.gif)

That's all my friends. As you can see the IDE give you many options to make it easier to develop Java application. But to learn the basics and to create console application we just need a text editor and the terminal. See you later!
