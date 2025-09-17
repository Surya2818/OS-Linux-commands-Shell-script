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
<img width="291" height="197" alt="1" src="https://github.com/user-attachments/assets/9997a290-b95b-4340-a4ee-59e9b557dfd4" />



cat < file2
## OUTPUT
<img width="293" height="165" alt="1 2" src="https://github.com/user-attachments/assets/cb57a5e0-83db-4493-8928-994b3380febe" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="401" height="68" alt="1 3" src="https://github.com/user-attachments/assets/3531352a-219d-4cf2-a69e-e316071f6af9" />
 
comm file1 file2
 ## OUTPUT
<img width="381" height="227" alt="1 4" src="https://github.com/user-attachments/assets/aa6118de-eda4-4c17-9c88-f5171669900a" />

 
diff file1 file2
## OUTPUT
<img width="338" height="272" alt="1 5" src="https://github.com/user-attachments/assets/9df4abdc-d0b8-4259-bd9b-bec655b3f5bf" />


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
<img width="311" height="91" alt="1 6" src="https://github.com/user-attachments/assets/729de716-a8e2-4b41-8d7b-ecdc6440c5fa" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="420" height="122" alt="1 7" src="https://github.com/user-attachments/assets/2543ec02-e336-421d-9838-ce26fab9f996" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="282" height="91" alt="1 8" src="https://github.com/user-attachments/assets/980651b2-5c85-4e3c-8c8d-ed83cf206891" />


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
<img width="342" height="117" alt="1 9" src="https://github.com/user-attachments/assets/230dc87c-dcbf-4cec-be4c-04879f05aae1" />



grep hello newfile 
## OUTPUT
<img width="377" height="122" alt="1 10" src="https://github.com/user-attachments/assets/639f595a-d790-45db-93d2-dee573fba0b1" />




grep -v hello newfile 
## OUTPUT
<img width="296" height="92" alt="1 11" src="https://github.com/user-attachments/assets/adddf718-d515-43ae-9e26-2f7186071ada" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="293" height="71" alt="1 12" src="https://github.com/user-attachments/assets/ccf927f6-1c36-43a3-8575-d101a272422c" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="300" height="72" alt="1 13" src="https://github.com/user-attachments/assets/b9e88085-ebe2-454a-89fe-d9a4d9c7078e" />




grep -R ubuntu /etc
## OUTPUT
<img width="307" height="73" alt="1 14" src="https://github.com/user-attachments/assets/125c919e-1391-4bba-b755-8ebe8eda55d5" />



grep -w -n world newfile   
## OUTPUT
<img width="420" height="95" alt="1 15" src="https://github.com/user-attachments/assets/42ff2d5b-e642-4df9-8819-b10ea82e14d5" />


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
<img width="463" height="82" alt="1 16" src="https://github.com/user-attachments/assets/c888817e-ec2a-4537-a43f-415438418d56" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1492" height="946" alt="1 17" src="https://github.com/user-attachments/assets/29cecb2c-48cc-4e59-95e3-ccae3707236a" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="377" height="112" alt="1 18" src="https://github.com/user-attachments/assets/d476955a-1b5e-4f44-a796-d2f558f21c08" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="406" height="178" alt="1 19" src="https://github.com/user-attachments/assets/5e2f1451-0be8-4c11-9f0d-87efd74185e3" />



egrep '(world$)' newfile 
## OUTPUT
<img width="457" height="92" alt="1 20" src="https://github.com/user-attachments/assets/b2d82bdd-11cc-492a-8afb-54b256900e0c" />



egrep '(World$)' newfile 
## OUTPUT
<img width="405" height="96" alt="1 21" src="https://github.com/user-attachments/assets/1c3f57b2-ad43-4624-95c8-9ff73368922d" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="405" height="96" alt="1 22" src="https://github.com/user-attachments/assets/9ea5544e-4478-4186-a0ba-9614dd4d54ae" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="360" height="78" alt="1 23" src="https://github.com/user-attachments/assets/858f0387-88ba-4642-b561-792518bdc55f" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="405" height="81" alt="image" src="https://github.com/user-attachments/assets/bc823be9-626e-4c29-a753-f3ad9e2085a2" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="417" height="77" alt="image" src="https://github.com/user-attachments/assets/9673b991-7b65-4a19-9b07-c5f309779432" />


egrep l{2} newfile
## OUTPUT
<img width="396" height="103" alt="image" src="https://github.com/user-attachments/assets/582e3ee6-3cdc-454d-a1ec-e893e9d8a71e" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="397" height="128" alt="image" src="https://github.com/user-attachments/assets/8cffda02-f25e-438e-a07a-80cf79ab8fe7" />


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
<img width="372" height="87" alt="image" src="https://github.com/user-attachments/assets/3b138970-321c-4561-8501-800d86955056" />



sed -n -e '$p' file23
## OUTPUT
<img width="528" height="81" alt="image" src="https://github.com/user-attachments/assets/3d7a9fc8-1294-4190-b454-76711f303a35" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="570" height="232" alt="image" src="https://github.com/user-attachments/assets/8e5e315a-00cf-45fc-981d-33bab91509dc" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="585" height="226" alt="image" src="https://github.com/user-attachments/assets/b15e96cf-1dc3-45ee-872d-53f732593627" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="587" height="231" alt="image" src="https://github.com/user-attachments/assets/2fed0a44-0f12-47dc-8ac3-bc082be5d1cf" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="457" height="173" alt="image" src="https://github.com/user-attachments/assets/8e700e5f-ca17-421c-b55b-cac1c4a5c229" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="415" height="132" alt="image" src="https://github.com/user-attachments/assets/3909bda4-4509-4236-98f7-9d9d80bc5727" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="380" height="95" alt="image" src="https://github.com/user-attachments/assets/8beb7ce9-34c9-4c30-84e2-55268b79bd2f" />



seq 10 
## OUTPUT
<img width="402" height="287" alt="image" src="https://github.com/user-attachments/assets/c475ad2d-d9ea-4235-a394-c5ad95244c99" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="377" height="128" alt="image" src="https://github.com/user-attachments/assets/eea61c20-69b5-42e8-8795-05222fe69d24" />



seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT
<img width="365" height="132" alt="image" src="https://github.com/user-attachments/assets/b0a0c9e4-dbba-464c-860d-8351e1c24506" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="358" height="127" alt="image" src="https://github.com/user-attachments/assets/5c7a6e1e-5049-4492-9a97-d15d82105166" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="417" height="127" alt="image" src="https://github.com/user-attachments/assets/740e6fbc-7b51-4468-a6d6-6ac1e42fa81a" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="532" height="128" alt="image" src="https://github.com/user-attachments/assets/98f94633-c523-4732-ab3b-856850a471a7" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="505" height="122" alt="image" src="https://github.com/user-attachments/assets/e0712dc6-bf8a-467f-824a-8591b76154c2" />



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
<img width="412" height="165" alt="image" src="https://github.com/user-attachments/assets/d87c4623-66ff-41c4-a8f8-13199d7034ee" />


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
<img width="417" height="133" alt="image" src="https://github.com/user-attachments/assets/2403402a-2030-4e03-b516-d8de2962186c" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="607" height="257" alt="image" src="https://github.com/user-attachments/assets/83450a64-3c37-45aa-8e0d-cbf3b845ffdb" />

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
<img width="517" height="97" alt="image" src="https://github.com/user-attachments/assets/b00c7848-4c20-4881-90ee-30268a7fcaeb" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="558" height="110" alt="image" src="https://github.com/user-attachments/assets/8ba296c3-d772-4931-887f-c1a693063d74" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="502" height="271" alt="image" src="https://github.com/user-attachments/assets/50213d73-2f33-41a0-8081-e433b8ec873c" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="691" height="286" alt="image" src="https://github.com/user-attachments/assets/03756840-9279-42cf-b390-99f00edbe911" />


tar -xvf backup.tar
## OUTPUT
<img width="557" height="268" alt="image" src="https://github.com/user-attachments/assets/d0164f60-d66c-4954-9e3c-da56b4ce4b67" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="640" height="102" alt="image" src="https://github.com/user-attachments/assets/67906338-426f-46bd-b252-052dd97ec94a" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="533" height="82" alt="image" src="https://github.com/user-attachments/assets/da7ec0fc-f434-47f5-b905-9f09b91d3ede" />

 

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="472" height="232" alt="image" src="https://github.com/user-attachments/assets/b891da4f-6013-4239-b34d-ca9ba3a1d162" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="421" height="317" alt="image" src="https://github.com/user-attachments/assets/59b7a742-5e64-4afe-ab6e-4790a3bf5546" />


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
<img width="490" height="775" alt="image" src="https://github.com/user-attachments/assets/4654777b-6335-46c2-9507-cf24bc6c12ed" />

 
ls file1
## OUTPUT
<img width="297" height="77" alt="image" src="https://github.com/user-attachments/assets/2715a3ea-6f7e-4dce-a218-e32d46085faa" />

echo $?
## OUTPUT 
<img width="267" height="81" alt="image" src="https://github.com/user-attachments/assets/003879fc-d174-43cf-8d1b-e4342f24515d" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="335" height="155" alt="image" src="https://github.com/user-attachments/assets/5852a517-af18-4d68-978b-4809e7cc0aca" />


 
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
## OUTPUT

<img width="363" height="277" alt="image" src="https://github.com/user-attachments/assets/9b2089f1-628c-4cae-9854-31ab00541e89" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="620" height="151" alt="image" src="https://github.com/user-attachments/assets/4e939222-b1ad-444d-91bf-c0fa9d845404" />



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
<img width="612" height="303" alt="image" src="https://github.com/user-attachments/assets/a5965dac-a477-4f5b-ad42-ca4667df33fb" />

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
<img width="530" height="582" alt="image" src="https://github.com/user-attachments/assets/1883a8ba-3038-4f67-910f-533b1efb5350" />



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
## OUTPUT
<img width="530" height="582" alt="Screenshot 2025-08-18 131157" src="https://github.com/user-attachments/assets/3d0aa2af-53cd-4248-a587-f18e9dec045d" />


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
## OUTPUT
<img width="517" height="680" alt="image" src="https://github.com/user-attachments/assets/fc05d88c-cff5-47bb-9193-361ff6011740" />

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
<img width="581" height="347" alt="image" src="https://github.com/user-attachments/assets/139a07bd-6224-4ca4-92bb-791af55ad473" />

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
 <img width="612" height="598" alt="image" src="https://github.com/user-attachments/assets/cd4ee855-d48e-4825-9307-7fc745ae7862" />

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
<img width="343" height="610" alt="image" src="https://github.com/user-attachments/assets/6432cc9b-2986-4ee8-a439-c80e0e9bd337" />

 
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
 <img width="306" height="452" alt="image" src="https://github.com/user-attachments/assets/c77dbf53-eac6-420c-b0e8-0307f0d80e87" />

 
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
<img width="655" height="456" alt="image" src="https://github.com/user-attachments/assets/b06f5854-1e34-4465-a145-d68acf689314" />

 
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
## OUTPUT
<img width="576" height="456" alt="image" src="https://github.com/user-attachments/assets/af123c85-c075-449a-8a66-cb9fe4230bf0" />

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
<img width="572" height="458" alt="image" src="https://github.com/user-attachments/assets/578b0c5e-67a7-4bb4-8832-4cf56c7c46cf" />

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
## OUTPUT
<img width="353" height="502" alt="image" src="https://github.com/user-attachments/assets/e7cc1615-98f7-4ccf-b9c2-ee8db36ca39e" />

$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="343" height="450" alt="image" src="https://github.com/user-attachments/assets/4cc623cc-7d35-4daf-8f43-fd5b8fa3f1e9" />


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
<img width="362" height="435" alt="image" src="https://github.com/user-attachments/assets/ab815431-d886-4e24-a34f-05179a1c9fd5" />

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
<img width="401" height="432" alt="image" src="https://github.com/user-attachments/assets/c01b2e37-9b22-4b14-a35b-84df4749dac4" />

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
<img width="360" height="701" alt="image" src="https://github.com/user-attachments/assets/94048ada-f4c3-4632-9e13-c1f04167b3e7" />

 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

## OUTPUT
<img width="361" height="505" alt="image" src="https://github.com/user-attachments/assets/11800f6c-c3e4-4851-96a3-9915b2e18fe3" />

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
<img width="553" height="558" alt="image" src="https://github.com/user-attachments/assets/f12ce289-f938-40ae-9870-fb589a5fe0c8" />

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
<img width="460" height="330" alt="image" src="https://github.com/user-attachments/assets/348dddba-1869-4731-a833-9d733fc71b30" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT
<img width="446" height="330" alt="image" src="https://github.com/user-attachments/assets/d3dc8b42-e6c4-46a3-a6eb-442575021f32" />




 
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
./funcex.sh 
## OUTPUT
<img width="577" height="526" alt="image" src="https://github.com/user-attachments/assets/ac94d21f-b743-4c89-9d75-5a851f0e796c" />


 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT
<img width="302" height="357" alt="image" src="https://github.com/user-attachments/assets/1f76e1b3-21a6-40f0-8fa3-5aa65f48a7ee" />


 
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
$ ./argshift.sh 1 2 3
## OUTPUT
<img width="396" height="483" alt="image" src="https://github.com/user-attachments/assets/a54ec90f-4589-4f98-892e-a7222723458e" />


 
cat argshift2.sh
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
 ./argshift2.sh 1 2 3
 <img width="338" height="678" alt="image" src="https://github.com/user-attachments/assets/415d0981-3964-4a92-9a95-e27f6f5cf993" />

 
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
 <img width="368" height="380" alt="image" src="https://github.com/user-attachments/assets/2d29e341-9440-41fa-beaa-94a5f96738b1" />

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
<img width="340" height="180" alt="image" src="https://github.com/user-attachments/assets/78b54a02-111c-4e80-85b8-0db16b2afc84" />


# RESULT:
The Commands are executed successfully.
