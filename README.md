<img width="359" height="76" alt="image" src="https://github.com/user-attachments/assets/3dcd4dba-f467-4dd8-97b4-f11e1a6cf9fe" /># OS-Linux-commands-Shell-scripting
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

<img width="231" height="147" alt="image" src="https://github.com/user-attachments/assets/8e6be6e0-0170-42c7-a998-67ef8293fab5" />


cat < file2
## OUTPUT

<img width="225" height="163" alt="image" src="https://github.com/user-attachments/assets/90eb1e0f-012c-43f5-aec8-57d86615f530" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="370" height="72" alt="image" src="https://github.com/user-attachments/assets/b33a41cb-2765-4582-a9c8-db5737882299" />

 
comm file1 file2
 ## OUTPUT

<img width="377" height="221" alt="image" src="https://github.com/user-attachments/assets/fbe27b30-c779-4a9a-a446-4b62da36ca25" />

 
diff file1 file2
## OUTPUT

<img width="322" height="264" alt="image" src="https://github.com/user-attachments/assets/c03f742a-32fa-4f78-b8be-395fa7cd9796" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

<img width="286" height="100" alt="image" src="https://github.com/user-attachments/assets/5ecdb470-b429-4fa6-ac8d-22d52a1c5709" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="353" height="124" alt="image" src="https://github.com/user-attachments/assets/f540a255-e094-419f-a640-f99c38703267" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="338" height="123" alt="image" src="https://github.com/user-attachments/assets/671b9a27-56a6-481b-afdc-d49dfcc3872d" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="288" height="74" alt="image" src="https://github.com/user-attachments/assets/33038532-f276-4997-acb4-6502ba4f980c" />


grep hello newfile 
## OUTPUT

<img width="281" height="72" alt="image" src="https://github.com/user-attachments/assets/fb97ac55-f099-408a-877a-c601aead875c" />



grep -v hello newfile 
## OUTPUT

<img width="312" height="73" alt="image" src="https://github.com/user-attachments/assets/2c15ad95-e4fa-4fcf-be99-2fe4a1ac318e" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="370" height="100" alt="image" src="https://github.com/user-attachments/assets/47ad7216-a164-498e-b60b-413b67908e0b" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="423" height="74" alt="image" src="https://github.com/user-attachments/assets/0c627717-4478-4615-9d1d-11a1a4ce23cf" />



grep -R ubuntu /etc
## OUTPUT

<img width="1433" height="394" alt="image" src="https://github.com/user-attachments/assets/07f6ecb6-62ee-4db6-9ead-cfedf0fb5944" />


grep -w -n world newfile   
## OUTPUT

<img width="329" height="89" alt="image" src="https://github.com/user-attachments/assets/9cf76390-cd81-4b69-8980-ab4fa2467fef" />


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

<img width="395" height="94" alt="image" src="https://github.com/user-attachments/assets/9efc1f9f-82c3-449c-93e1-9efa53fca83f" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="401" height="95" alt="image" src="https://github.com/user-attachments/assets/ad9876be-d232-472e-9d72-8abafd890262" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="418" height="95" alt="image" src="https://github.com/user-attachments/assets/3a1a4858-fcf3-49ea-a494-ee7360caa813" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="342" height="72" alt="image" src="https://github.com/user-attachments/assets/382e19f7-76e4-4bd3-bfa3-c67b76473e17" />



egrep '(world$)' newfile 
## OUTPUT


<img width="334" height="100" alt="image" src="https://github.com/user-attachments/assets/5e66da4c-8aa3-48b2-95a5-45932836473c" />


egrep '(World$)' newfile 
## OUTPUT

<img width="359" height="76" alt="image" src="https://github.com/user-attachments/assets/0ca924b8-6f8d-4c1c-80a6-fa72b25eca42" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="408" height="121" alt="image" src="https://github.com/user-attachments/assets/52430f89-c371-4651-a38d-f62d440508c8" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="367" height="71" alt="image" src="https://github.com/user-attachments/assets/0feabf7d-3759-489a-ac4a-df712e389bd5" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="447" height="78" alt="image" src="https://github.com/user-attachments/assets/6136fc2d-38a3-432c-9ea2-73a41e2f65ab" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="386" height="74" alt="image" src="https://github.com/user-attachments/assets/5a258b11-e244-49c5-9791-ca7a377aa2ba" />


egrep l{2} newfile
## OUTPUT

<img width="307" height="95" alt="image" src="https://github.com/user-attachments/assets/737b4ef8-cf31-4f90-8e15-7df4453170e8" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="386" height="123" alt="image" src="https://github.com/user-attachments/assets/4460cf2c-a374-48b1-b778-e85490d2aeb0" />


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


sed -n -e '3p' file23
## OUTPUT

<img width="354" height="77" alt="image" src="https://github.com/user-attachments/assets/8784fa7d-7fb4-41ed-b80a-dc5574a4963a" />


sed -n -e '$p' file23
## OUTPUT

<img width="368" height="74" alt="image" src="https://github.com/user-attachments/assets/a41b6cc7-89a1-4cce-97bd-e4545e20c9ad" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="426" height="243" alt="image" src="https://github.com/user-attachments/assets/b1a95c87-c693-4537-b399-2f946404a68d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="356" height="245" alt="image" src="https://github.com/user-attachments/assets/63091462-55bf-4f09-9798-1b2501c6cc00" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="486" height="244" alt="image" src="https://github.com/user-attachments/assets/9d01dee4-f017-433b-9ad6-eb51b314204e" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="382" height="175" alt="image" src="https://github.com/user-attachments/assets/0b390a90-a585-4982-a84f-19833b865705" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="382" height="175" alt="image" src="https://github.com/user-attachments/assets/86e826cf-7fcb-405e-b977-d94fe27f2bb7" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="424" height="120" alt="image" src="https://github.com/user-attachments/assets/dbe6d807-6226-4d69-ac60-5c875f86ae63" />


seq 10 
## OUTPUT

<img width="298" height="293" alt="image" src="https://github.com/user-attachments/assets/3bf592b0-e112-4e15-bb93-5b01e8ed7813" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="318" height="115" alt="image" src="https://github.com/user-attachments/assets/add6910f-4f0d-44a3-a03f-d6667b3d560f" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="363" height="116" alt="image" src="https://github.com/user-attachments/assets/ef66a0b9-428e-48f7-ad8c-1824c386b48a" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="339" height="143" alt="image" src="https://github.com/user-attachments/assets/00267f4d-be12-4870-aef0-4a5ebc15ce0a" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="300" height="118" alt="image" src="https://github.com/user-attachments/assets/105639be-7fa8-4767-bc76-2507dc5b5349" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="356" height="115" alt="image" src="https://github.com/user-attachments/assets/383baebf-b63c-46ac-8a13-e26b8735f8b8" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="417" height="122" alt="image" src="https://github.com/user-attachments/assets/78fecd20-64fe-47d3-bac3-0c4e2d89d03a" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="421" height="125" alt="image" src="https://github.com/user-attachments/assets/c971974e-9978-4b4b-a62a-64eba8ede081" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT

<img width="353" height="170" alt="image" src="https://github.com/user-attachments/assets/4c0453e1-3374-4549-9e63-8cc9b99b2df3" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

<img width="461" height="340" alt="image" src="https://github.com/user-attachments/assets/fb173b61-c3c1-4f04-bec9-d101a58b0eea" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="531" height="240" alt="image" src="https://github.com/user-attachments/assets/68de42c0-6634-429a-b979-d390096a7fe8" />


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
cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="388" height="123" alt="image" src="https://github.com/user-attachments/assets/b0976478-f5c6-46e4-95ab-e342fc70708c" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="498" height="121" alt="image" src="https://github.com/user-attachments/assets/eb8e5174-92f9-4d9d-b180-c924aa3f43b0" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="579" height="403" alt="image" src="https://github.com/user-attachments/assets/ca0afd68-7a28-4cd5-8f5b-98b46c48ca53" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="972" height="504" alt="image" src="https://github.com/user-attachments/assets/ec0b542c-dfa3-4360-b752-aeca10e63420" />



tar -xvf backup.tar
## OUTPUT

<img width="550" height="433" alt="image" src="https://github.com/user-attachments/assets/26da112c-025f-474f-ae7c-096922193b8d" />


gzip backup.tar

ls .gz
## OUTPUT

<img width="405" height="76" alt="image" src="https://github.com/user-attachments/assets/bd5aaef0-69fa-46dd-97ac-7d483a8c3bda" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="1632" height="128" alt="image" src="https://github.com/user-attachments/assets/d2b4069b-51ec-41ee-a7b2-bb1cdb745c53" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="453" height="224" alt="image" src="https://github.com/user-attachments/assets/fbedbe50-0b84-4d69-a309-362a6a39db89" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="432" height="128" alt="image" src="https://github.com/user-attachments/assets/59a4b512-083d-49d2-bd3a-2101107b5599" />


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
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

<img width="797" height="437" alt="image" src="https://github.com/user-attachments/assets/fd1e437b-83a0-4391-918b-d002780a99cc" />

 
ls file1
## OUTPUT

<img width="293" height="74" alt="image" src="https://github.com/user-attachments/assets/fd7fdac4-8956-47a1-855c-b44938608280" />


echo $?
## OUTPUT 

<img width="361" height="71" alt="image" src="https://github.com/user-attachments/assets/357e661f-68c2-4d14-a065-364f60f4b46e" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="272" height="77" alt="image" src="https://github.com/user-attachments/assets/d60b945d-c470-41fd-a402-9e783dfc6ff8" />

 
abcd
 
echo $?
 ## OUTPUT
<img width="361" height="71" alt="image" src="https://github.com/user-attachments/assets/926a6baa-d220-498c-a432-6051bb7fa98d" />


 
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

<img width="432" height="257" alt="image" src="https://github.com/user-attachments/assets/301a3f48-1ee4-476d-86db-d2b7320e4ddc" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="692" height="152" alt="image" src="https://github.com/user-attachments/assets/32067886-ee6d-4e5f-bcd0-ff03f1aa6467" />


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

<img width="613" height="166" alt="image" src="https://github.com/user-attachments/assets/c4ea1856-0468-4f8d-b48d-bfc38ee14074" />

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

<img width="610" height="247" alt="image" src="https://github.com/user-attachments/assets/83fa45cf-72c1-4c8e-836a-971cb6b7a614" />


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

<img width="651" height="212" alt="image" src="https://github.com/user-attachments/assets/d51827c5-990e-4ada-8768-7431f24a7991" />


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

<img width="690" height="193" alt="image" src="https://github.com/user-attachments/assets/ab30749f-d767-4789-a8b5-b2b6783e2559" />


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

<img width="702" height="152" alt="image" src="https://github.com/user-attachments/assets/97c0eb00-e384-48af-952b-02465c99b354" />


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

<img width="693" height="145" alt="image" src="https://github.com/user-attachments/assets/ebe0ef29-cf55-476e-9af1-d1c346a6740f" />


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
 ## OUTPUT

 
 <img width="357" height="117" alt="image" src="https://github.com/user-attachments/assets/500d930c-149a-413d-98f8-96da0c90b6de" />

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
 ## OUTPUT 
 
 <img width="366" height="339" alt="image" src="https://github.com/user-attachments/assets/db27e054-3e12-4ade-b240-76d16298854e" />

 
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
 
 ## OUTPUT
 <img width="527" height="171" alt="image" src="https://github.com/user-attachments/assets/00b93cbe-b32a-4422-bd3d-91ae89b0cbd1" />

 
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

 ## OUTPUT
 
 <img width="658" height="242" alt="image" src="https://github.com/user-attachments/assets/c726f124-c2ce-4d1f-b991-fda22fe90009" />

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
## OUTPUT

<img width="653" height="216" alt="image" src="https://github.com/user-attachments/assets/a80d7e4a-0c7a-41c2-a6b2-19267ea6b73f" />

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
 ## OUTPUT

 <img width="584" height="246" alt="image" src="https://github.com/user-attachments/assets/3e6bafc2-be65-40d7-a493-b1aab95d7915" />

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

<img width="364" height="220" alt="image" src="https://github.com/user-attachments/assets/faf3c9ae-0693-4b3f-9bd3-94a2f98606f2" />


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

<img width="235" height="173" alt="image" src="https://github.com/user-attachments/assets/dd0c90fe-d015-4c71-961c-9e8f3fc95d32" />

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

<img width="369" height="224" alt="image" src="https://github.com/user-attachments/assets/64e9eb4d-5f29-4058-a517-5d54fa119cc1" />

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

<img width="323" height="387" alt="image" src="https://github.com/user-attachments/assets/1520a423-9b83-419a-a4cb-a0821a3b709d" />

 
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

<img width="266" height="104" alt="image" src="https://github.com/user-attachments/assets/7c81f036-359a-4aae-8f63-c75aee72f428" />

 
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
 <img width="331" height="178" alt="image" src="https://github.com/user-attachments/assets/a5aadd50-3c82-48e4-8d2c-39669c0abc4c" />

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


<img width="610" height="166" alt="Screenshot 2025-09-22 085056" src="https://github.com/user-attachments/assets/24ecbeed-7759-4f60-b508-93a89617362e" />


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

 <img width="331" height="82" alt="image" src="https://github.com/user-attachments/assets/95c95fc2-44b4-41f1-be26-c0ef204c8697" />


 ./funcex.sh 1 2
 
<img width="274" height="81" alt="image" src="https://github.com/user-attachments/assets/d4fe7a96-7dbd-4cf0-9e8a-1f17cf38d968" />

 
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

<img width="309" height="127" alt="image" src="https://github.com/user-attachments/assets/35a0926c-3e41-407f-9288-3ef0a96eb276" />

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

 
 <img width="509" height="421" alt="image" src="https://github.com/user-attachments/assets/7e135e78-4f98-446a-abe2-04a025f50a5d" />

 
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
