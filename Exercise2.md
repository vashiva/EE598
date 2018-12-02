## Big ideas:

* Download gitkraken
* Download VMWare
* Download Ubuntu Desktop
* Download Chamapionship Branch Prediction 2016, evaluation data set, simulation infrastructure
* Get the VMWare setup with the Ubuntu Desktop
* Read about linux commands, simple ones for tar extraction:
` tar -xvf cbp2016.final.tar.gz `
* To do compression:
` tar -czf nameofcompressedfile.tar.gz file1.txt file2.trace file3.cpp file4.py `
* To do compiling, use make: all you need to do for projects already using make, is to use the command `make` in the directory of the project.
* For some projects, you may have to do `./configure.sh`
 * `make` followed by `make install`
 
 When ready:
 1. After compiling the sim folder with `make`, change the main.cc to output the trace instructions fed to the predictor.
 2. Declare a file variable, type ofstream, open the file.
 3. Where the branch predictor code is, there should be a call to Update Branch Predictor. Right before that, output to the file the hex for the Program counter followed by a space and a 0 or 1 for Not Taken and Taken.
 4. Compile and run it on a trace. To improve speed, you can comment out the predict and update predict, but you would need to modify code to not need the results of the prediction.
 
 
 ## Links

 ### C++
 * http://www.cplusplus.com/doc/tutorial/files/
 * https://stackoverflow.com/questions/1140995/build-an-linux-executable-using-gcc
 

 ### Apt Get
 * https://help.ubuntu.com/lts/serverguide/apt.html.en

 ### Make
 
 * https://robots.thoughtbot.com/the-magic-behind-configure-make-make-install
 
 ### Linux
 * https://files.fosswire.com/2007/08/fwunixref.pdf
 * https://github.com/luongvo209/Awesome-Linux-Software
 
 ### Markdown
 *  * https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
 
 ### Awesome list
 * On github, people posts "Awesome lists." These are lists of resources that relate to a specific subject. They even have a list of awesome lists:
 https://github.com/sindresorhus/awesome
 * https://github.com/search?q=awesome+list
 
 
 
