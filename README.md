
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

<img width="662" height="132" alt="image" src="https://github.com/user-attachments/assets/1e5d473e-2849-4738-b188-331828ee85a3" />


cat < file2
## OUTPUT

<img width="662" height="139" alt="image" src="https://github.com/user-attachments/assets/806de9e1-5e18-4ea8-9d63-391007655fe5" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="662" height="78" alt="image" src="https://github.com/user-attachments/assets/f9918524-86a5-4fd5-968a-6368a89bff93" />

 
comm file1 file2
 ## OUTPUT

<img width="662" height="270" alt="image" src="https://github.com/user-attachments/assets/70afd7d5-7f8d-4ba9-b1d6-a4f429d2bb75" />

 
diff file1 file2
## OUTPUT

<img width="662" height="270" alt="image" src="https://github.com/user-attachments/assets/19f4dd8b-cd96-4bff-991b-f80774497755" />


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

<img width="662" height="133" alt="image" src="https://github.com/user-attachments/assets/faf1a4ab-8685-4b0d-a1c0-aa774514047e" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="662" height="133" alt="image" src="https://github.com/user-attachments/assets/04061f23-8be4-47d6-8510-343f745c9372" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="662" height="133" alt="image" src="https://github.com/user-attachments/assets/a39d3f6a-4e85-4394-92e5-6536a8a268fe" />


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

<img width="662" height="81" alt="image" src="https://github.com/user-attachments/assets/4e19beb1-5710-4254-9617-a24ac8f96da9" />


grep hello newfile 
## OUTPUT

<img width="662" height="81" alt="image" src="https://github.com/user-attachments/assets/4fbf0948-6b8b-487f-a2d9-0cded253e98d" />



grep -v hello newfile 
## OUTPUT

<img width="662" height="81" alt="image" src="https://github.com/user-attachments/assets/ecc02cf2-7486-44e6-97a2-2cd2b1e16e6f" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="662" height="81" alt="image" src="https://github.com/user-attachments/assets/64998b95-0e0a-488e-95bb-d66149d5633c" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="662" height="81" alt="image" src="https://github.com/user-attachments/assets/65972321-05d8-4d6f-8651-fd80a883d71f" />



grep -R ubuntu /etc
## OUTPUT

<img width="662" height="134" alt="image" src="https://github.com/user-attachments/assets/0655de9f-bd0a-4b64-a18b-855b685e444c" />


grep -w -n world newfile   
## OUTPUT


<img width="662" height="84" alt="image" src="https://github.com/user-attachments/assets/f6534c1f-514f-4edc-9a95-27926d8401cb" />


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
<img width="662" height="84" alt="image" src="https://github.com/user-attachments/assets/c604ebdf-32a5-4b44-a34f-28a425cc5336" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="662" height="84" alt="image" src="https://github.com/user-attachments/assets/c3cd619e-8e3e-432d-8c38-0626f0b8bfaf" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="662" height="84" alt="image" src="https://github.com/user-attachments/assets/5e80a486-8009-4211-b896-0d273b72384d" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="662" height="84" alt="image" src="https://github.com/user-attachments/assets/ab40ff43-e826-42aa-943d-7c88628aec17" />



egrep '(world$)' newfile 
## OUTPUT


<img width="662" height="84" alt="image" src="https://github.com/user-attachments/assets/306926f0-12f0-43ce-88a5-ac8c45810de1" />


egrep '(World$)' newfile 
## OUTPUT

<img width="662" height="84" alt="image" src="https://github.com/user-attachments/assets/165ac6ce-c1b1-4582-91f7-cce929531ed7" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="662" height="97" alt="image" src="https://github.com/user-attachments/assets/d5344453-2d04-488a-90cc-925b243eb397" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="662" height="62" alt="image" src="https://github.com/user-attachments/assets/d64f3a12-e2cb-47c9-967d-6e8197a339c6" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="662" height="62" alt="image" src="https://github.com/user-attachments/assets/e27d84a1-d7f8-458f-8c02-eed2eb459928" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="662" height="62" alt="image" src="https://github.com/user-attachments/assets/ff0b2546-3d8c-45ca-a872-ab1b616bcaad" />


egrep l{2} newfile
## OUTPUT

<img width="662" height="78" alt="image" src="https://github.com/user-attachments/assets/5921a338-496f-4bcc-8606-db749d7bbead" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="662" height="98" alt="image" src="https://github.com/user-attachments/assets/dbff6a20-b4e7-42e8-b54c-aed905276509" />



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

<img width="662" height="98" alt="image" src="https://github.com/user-attachments/assets/1d65d9d7-ea1d-40c2-9365-5c7dfe1026f7" />


sed -n -e '$p' file23
## OUTPUT

<img width="662" height="98" alt="image" src="https://github.com/user-attachments/assets/43679527-56b4-43aa-96f9-05283816fe49" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="662" height="206" alt="image" src="https://github.com/user-attachments/assets/fd85aa8a-b4bd-43d3-b57e-1dda57f668fb" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="662" height="206" alt="image" src="https://github.com/user-attachments/assets/a2f5945b-8a18-457e-9695-b30588cb1458" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="662" height="206" alt="image" src="https://github.com/user-attachments/assets/93947b46-f631-41ea-936f-aa531c93de5c" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="662" height="135" alt="image" src="https://github.com/user-attachments/assets/d17dc078-98a5-47ae-b4e8-deb07437d174" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="662" height="98" alt="image" src="https://github.com/user-attachments/assets/216bb0ce-1aab-46d7-adff-c62484261ab8" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="662" height="83" alt="image" src="https://github.com/user-attachments/assets/cd5b444b-6fed-4e82-887b-6a0049bcf3f0" />


seq 10 
## OUTPUT

<img width="662" height="218" alt="image" src="https://github.com/user-attachments/assets/733fc544-a0a7-4c89-bd37-1e865dc2097d" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="662" height="98" alt="image" src="https://github.com/user-attachments/assets/25023f22-f412-4c25-953c-646d8d51098a" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="662" height="98" alt="image" src="https://github.com/user-attachments/assets/fbbcb0d4-db04-452e-bba0-7fc55b22e1f7" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="662" height="118" alt="image" src="https://github.com/user-attachments/assets/332c240b-dc00-4930-a91f-cc0828b74989" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="662" height="106" alt="image" src="https://github.com/user-attachments/assets/790602ca-a6a0-4385-9657-b46362145dcb" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="662" height="106" alt="image" src="https://github.com/user-attachments/assets/405847a5-0e74-44d0-8037-851faeab124a" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="662" height="106" alt="image" src="https://github.com/user-attachments/assets/1900b46c-6fad-4019-81a9-df4f218020ae" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="662" height="102" alt="image" src="https://github.com/user-attachments/assets/2f217b11-e635-471f-8f4f-ecd381824a9e" />


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

<img width="662" height="134" alt="image" src="https://github.com/user-attachments/assets/31dba3b9-917d-46ac-89ce-1b25f0972d98" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="662" height="183" alt="image" src="https://github.com/user-attachments/assets/4a412113-3ea1-47d8-aff7-500309adeb57" />


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

<img width="662" height="183" alt="image" src="https://github.com/user-attachments/assets/ecf30e90-e3c4-4bbf-92b8-91c65ee03775" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="662" height="183" alt="image" src="https://github.com/user-attachments/assets/0561a745-c6aa-4fd9-9ee0-7e5b65431235" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="662" height="321" alt="image" src="https://github.com/user-attachments/assets/5052f2c0-a5a7-4179-a3be-cc22ba2640a8" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="744" height="239" alt="image" src="https://github.com/user-attachments/assets/6934cb6b-4702-4716-a47f-22e079ea4ce5" />


tar -xvf backup.tar
## OUTPUT

<img width="662" height="363" alt="image" src="https://github.com/user-attachments/assets/e5d242ce-a52a-403d-9456-74e2111e5a02" />


gzip backup.tar

ls .gz
## OUTPUT

<img width="672" height="56" alt="image" src="https://github.com/user-attachments/assets/f84f5d63-dacf-4521-922c-5add358ff119" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="672" height="56" alt="image" src="https://github.com/user-attachments/assets/80c34f96-52fd-4663-88d4-c723d5935fef" />

 
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

cat herecheck.txt
## OUTPUT

<img width="672" height="90" alt="image" src="https://github.com/user-attachments/assets/19bfa608-5e90-48b0-8743-b664f418f667" />


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



<img width="672" height="327" alt="image" src="https://github.com/user-attachments/assets/6c23fb78-de43-4934-8f76-51668b508423" />

 
ls file1
## OUTPUT


<img width="672" height="60" alt="image" src="https://github.com/user-attachments/assets/1cde3d14-3465-46af-bb43-192a978f2e13" />


echo $?
## OUTPUT 


<img width="672" height="60" alt="image" src="https://github.com/user-attachments/assets/4132372e-adc8-4c67-8b27-93160a9eb727" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="672" height="60" alt="image" src="https://github.com/user-attachments/assets/f38c0772-9622-4b6c-9ceb-f0d834f446ec" />

 
abcd
 
echo $?
 ## OUTPUT
<img width="672" height="60" alt="image" src="https://github.com/user-attachments/assets/5ab28c01-4bbc-47eb-bd6c-d92a79609cc5" />


 
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

<img width="480" height="300" alt="image" src="https://github.com/user-attachments/assets/9f8e8c5d-d62e-46f7-9cb6-69ed891fd0c2" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="480" height="77" alt="image" src="https://github.com/user-attachments/assets/6be42644-97c1-4271-9550-c0997d750a19" />


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
<img width="557" height="213" alt="image" src="https://github.com/user-attachments/assets/c64be32b-c019-4ef8-8092-85590805eeea" />

<img width="557" height="76" alt="image" src="https://github.com/user-attachments/assets/cfca9c06-b2fe-4d4c-b2be-9ff678d37ba7" />


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

<img width="422" height="153" alt="image" src="https://github.com/user-attachments/assets/2b9a59fd-ff12-4db3-aaa2-1eed24d356b7" />


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

<img width="422" height="352" alt="image" src="https://github.com/user-attachments/assets/2498c29e-67b1-4ed1-9f7b-6ae3eb2e9c65" />


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

<img width="551" height="158" alt="image" src="https://github.com/user-attachments/assets/9b7aaf02-1b4e-4d20-afc0-e1487936b9cc" />


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

<img width="593" height="95" alt="image" src="https://github.com/user-attachments/assets/28082061-5b20-4506-bbad-9b7d3cb28e39" />



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

<img width="593" height="155" alt="image" src="https://github.com/user-attachments/assets/97b9ee4a-df5a-4942-b961-772cfe8ba270" />


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

 <img width="593" height="106" alt="image" src="https://github.com/user-attachments/assets/05004054-91db-4415-aa1f-1576b5861c8a" />

 
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
 
 <img width="593" height="242" alt="image" src="https://github.com/user-attachments/assets/fc6d052a-c8d2-4b91-8f8d-8c28aa26f0fe" />

 
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
 <img width="593" height="156" alt="image" src="https://github.com/user-attachments/assets/ada14d57-df16-4abf-96a7-0dad535e117c" />

 
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
 <img width="593" height="203" alt="image" src="https://github.com/user-attachments/assets/26c8a376-8d0b-4500-920f-374c5d12a837" />

 <
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
<img width="593" height="152" alt="image" src="https://github.com/user-attachments/assets/8916eaf8-a459-4fa6-8f79-b1b80806fc85" />


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

### OUTPUT
<img width="593" height="152" alt="image" src="https://github.com/user-attachments/assets/33fe1ff3-abca-4d8c-b035-5fd19d4d1207" />

 
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
<img width="593" height="210" alt="image" src="https://github.com/user-attachments/assets/c28439ae-7381-4530-87d7-422841c33019" />

 
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
<img width="593" height="183" alt="image" src="https://github.com/user-attachments/assets/25b5262f-e207-4108-a502-bf1d8443568a" />



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
<img width="593" height="183" alt="image" src="https://github.com/user-attachments/assets/0f7d19dc-ec0d-44d9-939a-c143ed26debc" />


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
<img width="593" height="154" alt="image" src="https://github.com/user-attachments/assets/4eafcf31-0daa-442d-a80f-2988f5fd302d" />


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
<img width="593" height="294" alt="image" src="https://github.com/user-attachments/assets/eba74b53-22b3-43cb-9e25-9edb4438968f" />


 
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

<img width="652" height="126" alt="image" src="https://github.com/user-attachments/assets/a1f66a9d-5ba8-4594-b210-210af602eea6" />

 
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
<img width="652" height="160" alt="image" src="https://github.com/user-attachments/assets/c9d8b4d7-aecd-4e53-bece-78d4be7308fb" />

 
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

 <img width="551" height="308" alt="image" src="https://github.com/user-attachments/assets/3a28b2b5-0e23-49e0-9527-f9ca6b185c2f" />

 
 
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
<img width="551" height="273" alt="image" src="https://github.com/user-attachments/assets/e12e67a8-89a1-498f-bc77-67fbe798d0b0" />


 
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
<img width="551" height="116" alt="image" src="https://github.com/user-attachments/assets/03dabcbd-e8b5-469c-a7ca-a3366a17ed96" />


# RESULT:
The Commands are executed successfully.
