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
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
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

<img width="350" height="147" alt="Screenshot 2026-07-29 084058" src="https://github.com/user-attachments/assets/aa9043eb-22fe-413f-ae11-beb969edd5de" />

cat < file2
## OUTPUT
<img width="396" height="172" alt="Screenshot 2026-07-29 084108" src="https://github.com/user-attachments/assets/0fc9f8b4-32cd-469b-997d-d5a0ed3781a7" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="431" height="121" alt="Screenshot 2026-07-29 084343" src="https://github.com/user-attachments/assets/f21654b1-e6e3-4584-9442-e9fac09aa2a5" />

comm file1 file2
 ## OUTPUT
<img width="428" height="257" alt="Screenshot 2026-07-29 084434" src="https://github.com/user-attachments/assets/b5a9cacc-a611-4337-8b20-9b576634a99a" />

 
diff file1 file2
## OUTPUT
<img width="481" height="331" alt="Screenshot 2026-07-29 084509" src="https://github.com/user-attachments/assets/bba68334-97dc-48b7-9bed-4058ba8352ae" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
<img width="481" height="331" alt="Screenshot 2026-07-29 084509" src="https://github.com/user-attachments/assets/22834a24-48af-4125-af08-252e16a1c123" />

cat > file22
<img width="457" height="160" alt="Screenshot 2026-07-29 085011" src="https://github.com/user-attachments/assets/4ff249fb-b8f3-43a1-9710-1850a724cd43" />




cut -c1-3 file11
## OUTPUT

<img width="416" height="120" alt="Screenshot 2026-07-29 085040" src="https://github.com/user-attachments/assets/a1eeb252-12fd-4f6b-a533-fc299d499d36" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="343" height="145" alt="Screenshot 2026-07-29 085132" src="https://github.com/user-attachments/assets/8519c727-b80c-4061-9020-b0352d9fe83c" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="467" height="175" alt="Screenshot 2026-07-29 085156" src="https://github.com/user-attachments/assets/6b039c0a-cdfd-449e-9172-50c8b5b093cd" />


cat < newfile 
<img width="313" height="157" alt="image" src="https://github.com/user-attachments/assets/d6e3ca35-4ad8-4bcb-befc-cdf38fc4e7ef" />

cat > newfile 
<img width="306" height="132" alt="image" src="https://github.com/user-attachments/assets/4a8547d2-f122-4ce4-889f-da3b43cb4b08" />

grep Hello newfile 
## OUTPUT

<img width="312" height="85" alt="image" src="https://github.com/user-attachments/assets/9aabae4d-2b4b-42c9-bd71-9ef18a16ce59" />


grep hello newfile 
## OUTPUT

<img width="312" height="87" alt="image" src="https://github.com/user-attachments/assets/4d2d94e3-7151-4c0f-9d05-f21c1f482052" />



grep -v hello newfile 
## OUTPUT
<img width="333" height="105" alt="image" src="https://github.com/user-attachments/assets/59f60d64-8f1b-44a6-89c8-9aa18075a832" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="396" height="107" alt="image" src="https://github.com/user-attachments/assets/5c503c87-4971-42a3-b650-49bc6bcf1011" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="445" height="82" alt="image" src="https://github.com/user-attachments/assets/fc29f0d1-39b8-43d5-8385-f9ecf409c018" />



grep -R ubuntu /etc
## OUTPUT
<img width="802" height="637" alt="image" src="https://github.com/user-attachments/assets/1eaa6fcc-b2a8-47b8-9413-c08a021b0a7d" />



grep -w -n world newfile   
## OUTPUT


cat < newfile 
<img width="320" height="175" alt="image" src="https://github.com/user-attachments/assets/ecec9c92-2683-42ab-8578-c962858502ec" />


cat > newfile
<img width="350" height="180" alt="image" src="https://github.com/user-attachments/assets/e1fd0170-fdf5-4f86-8398-56d01a93f905" />

egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="397" height="92" alt="image" src="https://github.com/user-attachments/assets/19e39982-f6f9-4b30-a9de-7e5101b346bb" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="382" height="132" alt="image" src="https://github.com/user-attachments/assets/f7567178-af9a-4036-b6e5-3407d0fce4a6" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="440" height="105" alt="image" src="https://github.com/user-attachments/assets/9b78aec8-2c10-4b03-8308-8c807baf6623" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="376" height="77" alt="image" src="https://github.com/user-attachments/assets/45ab4778-160d-4ee3-91d5-68678a8877e4" />



egrep '(world$)' newfile 
## OUTPUT
<img width="375" height="107" alt="image" src="https://github.com/user-attachments/assets/d27a8eb5-1487-4f5b-808a-d38155604cfb" />



egrep '(World$)' newfile 
## OUTPUT

<img width="351" height="76" alt="image" src="https://github.com/user-attachments/assets/f28be648-3b4f-4ada-ba57-392fb81c8de7" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="440" height="128" alt="image" src="https://github.com/user-attachments/assets/97effa08-8787-4b2a-b49b-fec0c69ae6d3" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="365" height="82" alt="image" src="https://github.com/user-attachments/assets/d8b01cc0-4ce7-4529-bf29-530dba7ddcef" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="427" height="81" alt="image" src="https://github.com/user-attachments/assets/e60564ba-c3d6-4fb2-98cb-055d8515c38e" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="417" height="85" alt="image" src="https://github.com/user-attachments/assets/3314bd3d-ab8b-4e0c-9dc0-237d2572d525" />


egrep l{2} newfile
## OUTPUT
<img width="357" height="107" alt="image" src="https://github.com/user-attachments/assets/d9ccc3da-2eb5-4ded-803b-1d675de44c3d" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="421" height="130" alt="image" src="https://github.com/user-attachments/assets/7fa98d47-99fd-484d-ab79-949a0a3129fb" />


cat > file23
<img width="448" height="258" alt="image" src="https://github.com/user-attachments/assets/c37629a2-44f7-467f-a80b-546ff4b17000" />




sed -n -e '3p' file23
## OUTPUT
<img width="363" height="86" alt="image" src="https://github.com/user-attachments/assets/11b246b6-5e58-4b69-bc85-71848c35d9af" />



sed -n -e '$p' file23
## OUTPUT

<img width="375" height="85" alt="image" src="https://github.com/user-attachments/assets/9a350e30-d058-4128-8d4d-54e8b71f791e" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="412" height="253" alt="image" src="https://github.com/user-attachments/assets/1a1efafc-7627-4a65-a7a6-ceecc7d4f5fa" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="393" height="256" alt="image" src="https://github.com/user-attachments/assets/002e171e-f011-4d7a-bcb8-945807fb71ba" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="406" height="245" alt="image" src="https://github.com/user-attachments/assets/bbc31660-697d-4d4d-aa3d-ac248bc91bbd" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="362" height="172" alt="image" src="https://github.com/user-attachments/assets/30efc2cc-9220-40a5-b909-e6fdbd351b26" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="425" height="127" alt="image" src="https://github.com/user-attachments/assets/1003c7bd-8b55-4531-854d-de86849996e0" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="443" height="97" alt="image" src="https://github.com/user-attachments/assets/8454cbba-7246-4df1-bb60-d8216f9f2b6e" />


seq 10 
## OUTPUT
<img width="342" height="293" alt="image" src="https://github.com/user-attachments/assets/46e5703c-6524-4c54-b4a5-191509842034" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="356" height="122" alt="image" src="https://github.com/user-attachments/assets/05ca2db9-700a-4bb7-9355-8d8f741e71c8" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="290" height="125" alt="image" src="https://github.com/user-attachments/assets/bdf6755a-f663-4de3-a0a0-2007e672cf22" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="357" height="157" alt="image" src="https://github.com/user-attachments/assets/1c9c47df-6f0c-4e19-ab4a-5f1b8374cf8e" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="377" height="141" alt="image" src="https://github.com/user-attachments/assets/ad5076b7-2147-4ad9-867a-a10a457a81c7" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="407" height="123" alt="image" src="https://github.com/user-attachments/assets/a9cbae2d-b631-4902-8487-e11428eccb11" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="410" height="132" alt="image" src="https://github.com/user-attachments/assets/62552080-960b-425c-8285-a11eb6505f1b" />


#Sorting File content
cat > file21
<img width="413" height="188" alt="image" src="https://github.com/user-attachments/assets/7882bd10-b303-4a8f-9338-95ac8e252cd6" />

sort file21
## OUTPUT
<img width="481" height="210" alt="image" src="https://github.com/user-attachments/assets/65829362-4cfb-4b6d-9abf-78084b49216b" />


cat > file22
<img width="347" height="215" alt="image" src="https://github.com/user-attachments/assets/4fa3fdac-e312-4abc-98ee-dc609abffd99" />

uniq file22
## OUTPUT
<img width="405" height="182" alt="image" src="https://github.com/user-attachments/assets/b98a314f-9c21-4a02-ae41-891797318c76" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="532" height="248" alt="image" src="https://github.com/user-attachments/assets/8307e4c2-a066-49dc-957d-070076a6901b" />

cat < urllist.txt
<img width="385" height="175" alt="image" src="https://github.com/user-attachments/assets/5889ff5c-9dc0-4ca4-b0b3-4a802b74eb31" />

cat > urllist.txt
<img width="376" height="165" alt="image" src="https://github.com/user-attachments/assets/690e43f8-94aa-4898-9d10-d75313e9f192" />

cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="422" height="176" alt="image" src="https://github.com/user-attachments/assets/5fd85f38-d35b-47e9-a7ae-f89b5c29c7a7" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="560" height="181" alt="image" src="https://github.com/user-attachments/assets/51aac949-dce5-480b-b854-2858f8af1787" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="816" height="603" alt="image" src="https://github.com/user-attachments/assets/3474e732-ebaf-4d41-9ed5-ff560ff7f3c2" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="835" height="552" alt="image" src="https://github.com/user-attachments/assets/82dc3fb4-5368-4058-af6e-be1f46b5505d" />

tar -xvf backup.tar
## OUTPUT
<img width="742" height="601" alt="image" src="https://github.com/user-attachments/assets/c5f417ab-63e8-4634-8dd6-2ed7e1af6703" />

 
# Shell Script

chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="513" height="152" alt="image" src="https://github.com/user-attachments/assets/78d97492-fc6d-40c4-aae5-8bbabaed4846" />


cat << stop > herecheck.txt
<img width="397" height="152" alt="image" src="https://github.com/user-attachments/assets/7376ba17-e8b0-47e3-99db-f212fa04bbcb" />


cat herecheck.txt
## OUTPUT
<img width="367" height="161" alt="image" src="https://github.com/user-attachments/assets/15d5ccbd-8f58-49d6-a0e9-9f538e09871c" />


cat < scriptest.sh 
<img width="428" height="465" alt="image" src="https://github.com/user-attachments/assets/2d1cd390-3267-43da-92df-919c85465e6e" />

 
<img width="375" height="117" alt="image" src="https://github.com/user-attachments/assets/e90a7f75-a42c-4d06-8ede-7d4337c3ec7c" />


 
ls file1
## OUTPUT
<img width="330" height="76" alt="image" src="https://github.com/user-attachments/assets/d0d3cd06-5b61-4603-8f17-d20e3aec6140" />

echo $?
## OUTPUT 
<img width="355" height="77" alt="image" src="https://github.com/user-attachments/assets/b2a3cd8d-62b3-40ad-8325-6c28fa5b7895" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="411" height="125" alt="image" src="https://github.com/user-attachments/assets/c3a4a685-4587-416b-844a-32305eb8e3da" />

abcd
 
echo $?
 ## OUTPUT
<img width="435" height="152" alt="image" src="https://github.com/user-attachments/assets/8cd2421f-f245-415e-b53d-5cc352a5a2e7" />


 
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
<img width="517" height="287" alt="image" src="https://github.com/user-attachments/assets/2d128d4f-2305-42c2-a87e-165617cb9e30" />


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

<img width="436" height="287" alt="image" src="https://github.com/user-attachments/assets/7274fc87-cb98-4dc7-adb7-c78008ac4921" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="622" height="165" alt="image" src="https://github.com/user-attachments/assets/2df4c953-371f-42af-8750-8ef35a96e3d4" />


# check file ownership
cat < psswdperm.sh 
<img width="627" height="302" alt="image" src="https://github.com/user-attachments/assets/77f2a609-f625-4714-a4e2-1879dd85fba1" />


cat psswdperm.sh 
<img width="602" height="260" alt="image" src="https://github.com/user-attachments/assets/220c6d1b-d47f-4def-824a-3b9f4143a515" />


## OUTPUT

# check if with file location
cat>ifnested.sh 
<img width="537" height="560" alt="image" src="https://github.com/user-attachments/assets/dcdd07dc-ba41-4e9e-883a-632ffd7b845d" />

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

<img width="580" height="517" alt="image" src="https://github.com/user-attachments/assets/3860e0af-521d-4720-8230-e6a617f8d8ae" />


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
<img width="626" height="175" alt="image" src="https://github.com/user-attachments/assets/93157c16-982b-4f63-98fd-be1ab3e21034" />

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
<img width="612" height="247" alt="image" src="https://github.com/user-attachments/assets/14733eeb-9937-4a16-811f-2e82d2a9b903" />

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
 
 <img width="645" height="495" alt="image" src="https://github.com/user-attachments/assets/d5c4ae97-4b2c-4b5c-b201-1ba0d862a826" />

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

<img width="592" height="612" alt="image" src="https://github.com/user-attachments/assets/ec25566a-9665-4a7d-8ba1-70afbaa1de78" />

# RESULT:
The Commands are executed successfully.
