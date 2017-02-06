# whopi #

### What ###

Whopi is a bash script that returns how many users are on each raspberry pi server at Michigan State University.

### Why ###

Whopi was created in response to a situation that arose in my computer architecture class at Michigan State University.  Our computer architecture class focuses on ARM processors, which are used on raspberry pis. We have 22 raspberry pis that that we can log onto from within the Engineering College's servers.  There is a webiste that displays how many people are on each pi, <http://www.cse.msu.edu/pie/kindex.php>. The website is there to allow people to pick a pi that has few or no users currently on it.  However, it was easy to see that people were not utilizing the site, as many people tended to use the pi named peach no matter what.  There were times when peach would be handling 10 users and almost every other pi was completely free.  It got to the point where the professor was sending out emails telling us to use something other than peach.  My solution: whopi.  With whopi, users can see how people are on each pi from any server that can connect to the raspberry pis.  This allows them to be able to easily see which pi they should use.

### Useage ###

Type 'whopi' in the command line to run the script.  By deafult, it will stop when it finds a pi with no users on it.  To see the user counts for every pi, use the option -a.

Whopi will be much more convenient if you have a public/private key pair that allows ssh to log onto a different server without prompting for the password each time.  Without the key pair, the user will have to enter their password for every pi that is checked.

Note: If whopi attempts to log onto a pi that you have not logged onto before, it will say the identity of the host cannot be establisned, and will ask you if you want to continue connecting.  My recommendation is to initially run whopi on all pis ("whopi -a") to get this out of the way for future uses.  

### Tasks ###

 - [x] Check every pi and print the results to standard output
 - [x] Automatically use the correct username for ssh connections
 - [ ] Implement a timeout for the pi connections for times when a pi is not responding quickly and display appropriate output
 - [ ] Implement a -h option that will display a help message in the terminal.  

### Release Date ###

First Release: 2/5/2016

### Author ###

Jared Clark
