# LAB 1
# How to login to course-specific account on ieng6 as in incoming 15L student on mac. 

**step one**
**if you already have it downloaded you can skip this step**
First you need to download vs code using this
[link](https://code.visualstudio.com/docs/setup/mac) 
* click yes and allow to everything then open when done downloading 
* once opened you should see this page or a version similar to this page 
* ![image](https://user-images.githubusercontent.com/122490992/211930806-81ff6071-c098-440e-9ed5-5c48c906b977.png)

**step two** 
- you now need to remotely connect by using the terminal which can be accesed from the toolbar when in visual code  as such 
   <img width="1187" alt="image" src="https://user-images.githubusercontent.com/122490992/211931672-6007ee51-e6cd-4828-b2f8-863255c7cc50.png">
- now in the terminal use ssh `cs15lwi23XXX@ieng6.ucsd.edu` in which you will have to replace the XXX with your specific account which will be found through here [link](https://sdacs.ucsd.edu/~icc/index.php)
- it will then prompt you if you want to continue connecting, to which you will say yes 
- then you will have enter a password in which you made through the link found from your specific account
- all of this in total should look as such 
- ![image](https://user-images.githubusercontent.com/122490992/211932210-9803b3a3-658e-449d-8464-e4a6f17ccfaf.png)

**step three** 
- have fun by using some commands in the remote server 
- see for yourself if some of them work such as cd, ls, pwd, mkdir, and cp
- cp `/home/linux/ieng6/cs15lwi23/public/hello.txt ~/`
- cat `/home/linux/ieng6/cs15lwi23/public/hello.txt`
- the ones that worked well for me personally were 
- ls -lat
- ls -a
- ls <directory> where <directory> is `/home/linux/ieng6/cs15lwi23/cs15lwi23XXX` , where the XXX is yours or anothers persons name 
- ![image](https://user-images.githubusercontent.com/122490992/211933220-aeb293ce-c6e1-479b-a043-7cfec648f8ac.png)
- you can then logout with exit 
   
**This was a very simple tuturial on how to gain remote access that I learned in person through lab 1.**
