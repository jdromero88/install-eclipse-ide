jodarove@linux-mint:~/development/code/blog/install-eclipse-ide(master)$ ls
hello-world.java  img  readme.md
jodarove@linux-mint:~/development/code/blog/install-eclipse-ide(master)$ javac hello-world.java

Command 'javac' not found, but can be installed with:

sudo apt install default-jdk            
sudo apt install openjdk-11-jdk-headless
sudo apt install ecj                    
sudo apt install openjdk-8-jdk-headless

jodarove@linux-mint:~/development/code/blog/install-eclipse-ide(master)$ ls
hello-world.java  img  readme.md
jodarove@linux-mint:~/development/code/blog/install-eclipse-ide(master)$ javac hello-world.java

Command 'javac' not found, but can be installed with:

sudo apt install default-jdk            
sudo apt install openjdk-11-jdk-headless
sudo apt install ecj                    
sudo apt install openjdk-8-jdk-headless

jodarove@linux-mint:~/development/code/blog/install-eclipse-ide(master)$ which java
/usr/bin/java
jodarove@linux-mint:~/development/code/blog/install-eclipse-ide(master)$ java -version
java version "1.8.0_261"
Java(TM) SE Runtime Environment (build 1.8.0_261-b12)
Java HotSpot(TM) 64-Bit Server VM (build 25.261-b12, mixed mode)
jodarove@linux-mint:~/development/code/blog/install-eclipse-ide(master)$ javac hello-world.java
hello-world.java:6: error: ';' expected
    System.out.println("Hello World!")
                                      ^
1 error
jodarove@linux-mint:~/development/code/blog/install-eclipse-ide(master)$ javac hello-world.java
jodarove@linux-mint:~/development/code/blog/install-eclipse-ide(master)$ ls
HelloWorld.class  hello-world.java  img  readme.md
jodarove@linux-mint:~/development/code/blog/install-eclipse-ide(master)$ java HelloWorld
Hello World!
