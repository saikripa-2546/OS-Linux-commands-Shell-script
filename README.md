# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="291" height="147" alt="image" src="https://github.com/user-attachments/assets/16f97a90-0fac-4c8c-a71b-fa696063e448" />



cat < file2
## OUTPUT
<img width="250" height="163" alt="image" src="https://github.com/user-attachments/assets/29689e47-ead0-458c-a4d9-50e79615f619" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="347" height="72" alt="image" src="https://github.com/user-attachments/assets/461cf8a0-2467-42bd-bf52-ba8b74b1f159" />

comm file1 file2
 ## OUTPUT
<img width="341" height="222" alt="image" src="https://github.com/user-attachments/assets/8b618cfd-7e94-4333-90d7-39be043884d8" />

 
diff file1 file2
## OUTPUT
<img width="352" height="275" alt="image" src="https://github.com/user-attachments/assets/dab72da7-55ff-42ca-9ddc-1d1c3d8cecdc" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
<img width="360" height="103" alt="image" src="https://github.com/user-attachments/assets/8b13e2ca-257a-430c-a42e-88926ded5eb9" />

cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
<img width="422" height="122" alt="image" src="https://github.com/user-attachments/assets/ce4df8b7-edc6-4a3e-9f36-6cc1f21571d5" />



cut -c1-3 file11
## OUTPUT
<img width="345" height="97" alt="image" src="https://github.com/user-attachments/assets/54226a67-cd42-4238-81e0-642848cf65c4" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="382" height="120" alt="image" src="https://github.com/user-attachments/assets/e7263a82-6dfe-49d2-8f40-a49554f67572" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="357" height="121" alt="image" src="https://github.com/user-attachments/assets/f25ee129-4709-43b0-ac4c-8c727705fd5c" />


cat < newfile 
```
Hello world
hello world
^d
````

cat > newfile 
Hello world
hello world

 ****<img width="290" height="101" alt="image" src="https://github.com/user-attachments/assets/8de63d94-72b9-4813-901b-5aacbbee4519" />

grep Hello newfile 
## OUTPUT
<img width="307" height="72" alt="image" src="https://github.com/user-attachments/assets/ef4a60f3-88b8-4c52-bfc9-0a3232ffd930" />



grep hello newfile 
## OUTPUT
<img width="328" height="72" alt="image" src="https://github.com/user-attachments/assets/bb1e4d24-3e0f-424d-904f-483616275d02" />




grep -v hello newfile 
## OUTPUT
<img width="317" height="72" alt="image" src="https://github.com/user-attachments/assets/92d43f42-489b-42d3-8994-ed7c14b9cc1c" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="397" height="97" alt="image" src="https://github.com/user-attachments/assets/83f5bc53-dce8-483b-bd6d-0c3cac44f3f4" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="413" height="70" alt="image" src="https://github.com/user-attachments/assets/8b7443d0-2dde-4654-85c9-e31d3bd258bf" />




grep -R ubuntu /etc
## OUTPUT
<img width="1483" height="935" alt="image" src="https://github.com/user-attachments/assets/be246d49-9a10-4cb7-9bf0-d3b5d57bd398" />
<img width="1411" height="936" alt="image" src="https://github.com/user-attachments/assets/00e96c3d-cff5-4a39-821a-7bf66cce2ee2" />
<img width="1656" height="933" alt="image" src="https://github.com/user-attachments/assets/b8aaf2e4-46c8-447f-89ba-6f3d3e479a77" />
<img width="1500" height="877" alt="image" src="https://github.com/user-attachments/assets/394ab0f9-e27c-43a0-9ec3-7d816eec0cd2" />



grep -w -n world newfile   
## OUTPUT
<img width="368" height="91" alt="image" src="https://github.com/user-attachments/assets/09d850ec-a7b2-44d1-9e04-8c083b467cee" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="378" height="96" alt="image" src="https://github.com/user-attachments/assets/848acfc0-7f20-4b2f-9350-80df9aa87506" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="375" height="92" alt="image" src="https://github.com/user-attachments/assets/01b11eaf-24e7-48e0-be81-848b4aaa5350" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="412" height="100" alt="image" src="https://github.com/user-attachments/assets/ef4edc3a-c804-422e-92ba-ab39011e96b7" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="323" height="67" alt="image" src="https://github.com/user-attachments/assets/515bdb72-c07d-4345-b0f4-65f9743d0eb5" />



egrep '(world$)' newfile 
## OUTPUT
<img width="331" height="92" alt="image" src="https://github.com/user-attachments/assets/ae9c7c4c-ddcb-475a-bfa7-39f1cea1be21" />



egrep '(World$)' newfile 
## OUTPUT
<img width="333" height="43" alt="image" src="https://github.com/user-attachments/assets/050d8769-9985-4b32-88e1-89693f5e3463" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="357" height="97" alt="image" src="https://github.com/user-attachments/assets/5f7bcc19-2b80-42a9-872c-d371da1a26b6" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="367" height="50" alt="image" src="https://github.com/user-attachments/assets/c5967211-e99b-4a55-84fd-08208f773cc1" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="372" height="51" alt="image" src="https://github.com/user-attachments/assets/b1b9ae03-eac5-49a9-a394-481e2ebe9875" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="372" height="51" alt="image" src="https://github.com/user-attachments/assets/57dbdeb3-2235-433b-a896-f9c63e92f6e0" />


egrep l{2} newfile
## OUTPUT
<img width="290" height="100" alt="image" src="https://github.com/user-attachments/assets/b2fa25a8-6fa5-46cb-9868-9b295c54c054" />



egrep 's{1,2}' newfile
## OUTPUT 


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```
<img width="408" height="268" alt="image" src="https://github.com/user-attachments/assets/80f73d9b-a06a-4105-83b6-07222c7366f3" />



sed -n -e '3p' file23
## OUTPUT
<img width="300" height="70" alt="image" src="https://github.com/user-attachments/assets/79ecc531-39f9-42b1-9e4d-754167c88ba4" />



sed -n -e '$p' file23
## OUTPUT
<img width="297" height="77" alt="image" src="https://github.com/user-attachments/assets/ec60ad9d-6498-4a6b-a0b7-aa192dc88dfe" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="362" height="248" alt="image" src="https://github.com/user-attachments/assets/9f9bf278-b5ea-46d6-bc7c-01a03405eb41" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="347" height="250" alt="image" src="https://github.com/user-attachments/assets/d3088674-8d9f-4a4f-a8b5-cd82d1560dac" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="385" height="243" alt="image" src="https://github.com/user-attachments/assets/ddd60372-5388-4053-9fab-3656fe8b99bd" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="352" height="168" alt="image" src="https://github.com/user-attachments/assets/60abe957-60ea-40f5-aa3d-38a650544899" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="395" height="116" alt="image" src="https://github.com/user-attachments/assets/cf1cdd09-f67e-4b15-b2d3-e9f14ba04369" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="397" height="100" alt="image" src="https://github.com/user-attachments/assets/1d158248-1db6-4bef-b050-9196f56a29af" />



seq 10 
## OUTPUT
<img width="313" height="292" alt="image" src="https://github.com/user-attachments/assets/40dc0c74-7e5a-4368-afd9-25a19fc71343" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="310" height="120" alt="image" src="https://github.com/user-attachments/assets/6dfdb4e8-fe34-4fd7-b7fc-e2475264b7c0" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="306" height="121" alt="image" src="https://github.com/user-attachments/assets/ed5ad39a-41a7-4d9c-9983-74b0394456c9" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="317" height="142" alt="image" src="https://github.com/user-attachments/assets/4e119546-d270-44e6-8ca0-3f92689dd926" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="316" height="120" alt="image" src="https://github.com/user-attachments/assets/f3bf2467-9a31-46c3-87cf-62252752a5d7" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="327" height="125" alt="image" src="https://github.com/user-attachments/assets/5680d0ad-57fb-4b38-9b93-50ac8cdf62f7" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="366" height="125" alt="image" src="https://github.com/user-attachments/assets/f23f415e-3492-4454-8b7f-e3ad484efe2b" />



sed -n '2,4{s/$/*/;p}' file23
<img width="365" height="126" alt="image" src="https://github.com/user-attachments/assets/028af757-6b55-4f6c-8c9a-ae23e6a87eb6" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
<img width="305" height="161" alt="image" src="https://github.com/user-attachments/assets/3312b3d8-3da1-4d1c-af96-bd1fb188b123" />

sort file21

## OUTPUT
<img width="295" height="168" alt="image" src="https://github.com/user-attachments/assets/75df7093-2430-49c7-80a0-6370f7bfeb8a" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
<img width="353" height="205" alt="image" src="https://github.com/user-attachments/assets/75691415-9375-49ca-90e9-4bdcae14aace" />

uniq file22
## OUTPUT
<img width="377" height="172" alt="image" src="https://github.com/user-attachments/assets/980baa1c-4c96-4818-8db9-f06458c708c1" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="590" height="235" alt="image" src="https://github.com/user-attachments/assets/e44f5325-55e7-4dc8-aad6-b136ff79cd8b" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
<img width="327" height="122" alt="image" src="https://github.com/user-attachments/assets/5f5c2307-5c9e-4e0a-b90f-207c950407cb" />

cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="348" height="118" alt="image" src="https://github.com/user-attachments/assets/4dee7f66-2ebb-49c4-8ed2-a2ee0f1570c8" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="455" height="123" alt="image" src="https://github.com/user-attachments/assets/e9f6348b-a9b9-4974-8af5-4c83f22039f3" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="758" height="907" alt="image" src="https://github.com/user-attachments/assets/d245cd0c-5263-4df2-a36a-7ca0ab23be70" />
<img width="468" height="651" alt="image" src="https://github.com/user-attachments/assets/5962c8ff-3f21-4f7e-ba30-60962d17f6e1" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="927" height="902" alt="image" src="https://github.com/user-attachments/assets/98226b2b-12ec-4b9a-ac93-c35ecc2db38f" />

<img width="868" height="725" alt="image" src="https://github.com/user-attachments/assets/eb2cfba2-d64e-40f2-83ea-e934755c97ea" />

tar -xvf backup.tar
## OUTPUT
<img width="802" height="872" alt="image" src="https://github.com/user-attachments/assets/0e8f31da-0f5e-4d87-913c-d6d157239057" />
<img width="611" height="552" alt="image" src="https://github.com/user-attachments/assets/6ea4ef32-ad01-416f-a145-1f1046bf9943" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1338" height="573" alt="image" src="https://github.com/user-attachments/assets/9f37251d-5bac-4b19-9e09-c002a9c15ae6" />

gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```
<img width="387" height="147" alt="image" src="https://github.com/user-attachments/assets/d901bbd9-3a2f-468b-82fa-6a945c1621a5" />


cat herecheck.txt
## OUTPUT
<img width="356" height="122" alt="image" src="https://github.com/user-attachments/assets/ca57944f-b8a8-414b-bd46-7a6c514d60ee" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```
<img width="412" height="352" alt="image" src="https://github.com/user-attachments/assets/73772da5-18b7-46f1-81b9-f3c3f156f868" />

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 <img width="372" height="327" alt="image" src="https://github.com/user-attachments/assets/015f5908-3a95-4a6f-978b-2a7baf20cadb" />

chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="762" height="427" alt="image" src="https://github.com/user-attachments/assets/209c0ca5-fae4-468d-927a-8e19b6d5e869" />

 
ls file1
## OUTPUT
<img width="317" height="73" alt="image" src="https://github.com/user-attachments/assets/b3708618-eed7-46df-81b7-2020fe27dc2b" />

echo $?
## OUTPUT 
<img width="290" height="72" alt="image" src="https://github.com/user-attachments/assets/7021ee1e-3b75-4ec0-886e-07ac5f2574d7" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="512" height="146" alt="image" src="https://github.com/user-attachments/assets/98d3a7e0-21fe-4d43-84f5-83d6ac887eac" />

abcd
 
echo $?
 ## OUTPUT
<img width="482" height="150" alt="image" src="https://github.com/user-attachments/assets/ff6966ed-64d0-432d-a34c-33b88eed4b7b" />


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.
