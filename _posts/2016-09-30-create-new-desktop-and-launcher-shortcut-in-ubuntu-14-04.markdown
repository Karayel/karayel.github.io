---
published: true
title: Create New Desktop and Launcher Shortcut in Ubuntu 14.04
layout: post
tags: [linux, shortcut]
categories: [linux]
---
### Create New Desktop Shortcut

1) Open Terminal.Type the below code in terminal and hit enter.
{% highlight bash %}
sudo apt-get install --no-install-recommends gnome-panel
{% endhighlight %}

2) Then type below code in terminal and hit enter
{% highlight bash %}
gnome-desktop-item-edit ~/Desktop/ --create-new
{% endhighlight %}

3) The create launcher window will pop-up,Type application name in the name field and type application name or path or browse in the command field. And click OK button.
![alt tag](http://i.stack.imgur.com/VqTEQ.png)

4) Now check your desktop for the shortcut.

### Create New Launcher Shortcut

1) In Create New Desktop Shortcut section, you created an desktop shortcut. Open the shortcut with text editor and copy it. 
{% highlight bash %}
#!/usr/bin/env xdg-open
[Desktop Entry]
Version=1.0
Type=Application
Terminal=false
Icon[en_US]=robomongo
Exec=/home/karayel/Programs/robomongo-0.9.0-rc10-linux-x86_64-33c89ea/bin/robomongo
Name[en_US]=RoboMongo
Name=RoboMongo
Icon=robomongo
{% endhighlight %}

2) Open Terminal. Type the below code in terminal and hit enter.
{% highlight bash %}
sudo nano /usr/share/applications/adt.desktop
{% endhighlight %}

3) Paste the code and save it.

4) Now you can see the application in applications.

5) Open and lock it the launcher. That's it.