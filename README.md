# Operating systems Lab exercise
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

chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d

cat > file2

anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d

### Display the content of the files
cat < file1
## OUTPUT
<img width="1581" alt="432240172-321fb4d1-b0f3-453e-8d18-fcbcabdfa5b0" src="https://github.com/user-attachments/assets/1a284ca1-7d6a-4602-bff2-e255de914af5" />



cat < file2
## OUTPUT
<img width="1581" alt="432240816-e650db97-a091-42f6-94f8-892510581cdb" src="https://github.com/user-attachments/assets/863970f5-adad-47de-b89c-cccac0060d1f" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="1593" alt="432241032-b036a974-5b96-4257-ad58-9a5574e21981" src="https://github.com/user-attachments/assets/c497af93-d9d4-40f5-b256-c6574b854bff" />

comm file1 file2
 ## OUTPUT
<img width="1581" alt="432241065-1a8901fa-f0c4-4cad-b210-22dc684ffba6" src="https://github.com/user-attachments/assets/e2f46a5e-54ac-4d63-bab4-d7a7ec1df535" />

 
diff file1 file2
## OUTPUT

<img width="1581" alt="432241141-7d1f7f21-0e2e-4f13-9e6d-bf6a03fbec3e" src="https://github.com/user-attachments/assets/297fc624-0111-44e1-a5a6-8c23f4a25bc6" />

#Filters

### Create the following files file11, file22 as follows:

cat > file11

Hello world
This is my world
^d

cat > file22

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d



cut -c1-3 file11
## OUTPUT

<img width="1581" alt="432241247-58fa2591-5c88-44c5-9282-b2e4716d867a" src="https://github.com/user-attachments/assets/74798dc2-7664-4270-8d72-fdd001f516bc" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="1669" alt="432241271-b8425d35-b16b-49eb-a164-5b04c945d5ec" src="https://github.com/user-attachments/assets/db01b1a7-e41f-4cfc-a4b2-a349d10e032c" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="1669" alt="432241332-15b5be2b-ee24-4449-b723-253f677c91d3" src="https://github.com/user-attachments/assets/76aa1ecb-ec69-4c0f-a116-22452a1ef7bf" />


cat < newfile 

Hello world
hello world
^d
`
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="1669" alt="432241531-5106f43e-2656-4646-9c09-2d0dffdefd71" src="https://github.com/user-attachments/assets/42c544ff-d647-4c73-9866-e18e6812577a" />



grep hello newfile 
## OUTPUT

<img width="1669" alt="432241571-cbaf8849-1b7c-46f8-87de-7a71203737a8" src="https://github.com/user-attachments/assets/2511cd56-ccf6-4931-b235-f31327ca00f8" />



grep -v hello newfile 
## OUTPUT

<img width="1669" alt="432241600-bfa3fa1f-7818-471b-87d5-583e62376032" src="https://github.com/user-attachments/assets/c9bb7261-0a12-4c58-ac37-eae500a945e3" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="1781" alt="432241626-358a1065-203f-447a-80f8-13eadbfe4dd2" src="https://github.com/user-attachments/assets/b36af6d5-a01e-428a-b3cc-559767bda9cc" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1827" alt="432241686-268e6be4-9a9e-4192-92c3-6cd8548ceda9" src="https://github.com/user-attachments/assets/a45cacd4-f8fe-49c8-826d-5b39502ef03e" />



grep -R ubuntu /etc
## OUTPUT

<img width="1039" alt="432241711-1f64bcc8-71b9-4f8a-81d0-203d5901f965" src="https://github.com/user-attachments/assets/6bef6009-15ba-4723-8af0-a8d9b25c3967" />


grep -w -n world newfile   
## OUTPUT
<img width="1108" alt="432241755-fce49f5f-eadd-46ec-b718-acaa9ee207a3" src="https://github.com/user-attachments/assets/582f446c-f899-4974-b35e-b4ea948b2bbd" />


cat < newfile 

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d


cat > newfile

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 
egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="1172" alt="432241797-90ddc705-6c97-4a46-af70-387223daf35a" src="https://github.com/user-attachments/assets/cf724528-3ef6-461e-aef2-c3c199e3ea79" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="1172" alt="432241837-32a27f75-ec39-453d-b72d-5fa6ef0fd89c" src="https://github.com/user-attachments/assets/c586e08a-1477-4094-a082-81fa6c905f8e" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="1191" alt="432241911-c0e048d5-def5-45d2-b5af-f199d58a913c" src="https://github.com/user-attachments/assets/6b698493-9451-4938-a985-8193bc01460e" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="1191" alt="432241957-af9d230b-7038-4dc0-a7b7-840fd2e4ac14" src="https://github.com/user-attachments/assets/007c80c6-a10c-4969-aad1-f2c9c0f73969" />



egrep '(world$)' newfile 
## OUTPUT

<img width="1191" alt="432242009-74d0d408-ab75-4faa-87bd-1de9df999e57" src="https://github.com/user-attachments/assets/53aab77e-9fb8-4d36-abf0-0192dec6df44" />


egrep '(World$)' newfile 

## OUTPUT
<img width="1191" alt="432242031-1296900e-e01c-4ffa-a731-d1f1a7ff7131" src="https://github.com/user-attachments/assets/b4d784aa-4f7b-425c-b36e-4aa236861d92" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1191" alt="432242031-1296900e-e01c-4ffa-a731-d1f1a7ff7131" src="https://github.com/user-attachments/assets/870b07a8-13c0-4435-af58-ecbdd1c21960" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="1191" alt="432242052-95b5e0e0-fb50-4aad-a26d-5f335ffadfd2" src="https://github.com/user-attachments/assets/58a6f9fb-39c3-481a-b85a-95e0c0643668" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1191" alt="432242111-0e2ea44c-3130-47ae-8d85-66fef3e84c55" src="https://github.com/user-attachments/assets/afd1c2ea-c335-4d93-9838-96afe71c9e41" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1191" alt="432242148-09e2c2ee-16f7-43f4-ae35-e6ae1bd1eb4b" src="https://github.com/user-attachments/assets/4e0be656-67bb-4533-8d39-089d62793a07" />


egrep l{2} newfile
## OUTPUT

<img width="1191" alt="432242177-9d36ba13-5431-4647-bc82-1196afce2024" src="https://github.com/user-attachments/assets/e5f6a4f0-2cf7-451e-b526-3f0554bdc952" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="1191" alt="432242331-e7b33ab0-b297-4786-bfec-550b89a4b7c4" src="https://github.com/user-attachments/assets/39b46b8f-eab7-4707-b055-fe90f3d5c7b6" />


cat > file23

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d



sed -n -e '3p' file23
## OUTPUT
<img width="1191" alt="432242369-7ce206ad-216a-4bd8-aa72-e4f0ac95e770" src="https://github.com/user-attachments/assets/50a27185-0a7e-40d2-8270-89bd55bbb1ad" />



sed -n -e '$p' file23
## OUTPUT

<img width="1191" alt="432242401-47770e6b-3c65-4015-8fd7-d2367829fcf3" src="https://github.com/user-attachments/assets/fbaa27da-3fdb-4f05-9039-dfa14f5ac3ac" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1191" alt="432242432-2d98ff67-5999-4434-bebc-d180f83728ff" src="https://github.com/user-attachments/assets/1e1dc163-03ea-4324-8c2c-14a944a534c2" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1191" alt="432242458-6bcc480c-daff-4679-8ff7-3e232b4271e1" src="https://github.com/user-attachments/assets/01b3b713-a4a7-4adf-9370-5f0e016bd720" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="1191" alt="432242483-0067d01f-6845-49df-b841-11b35b2605ce" src="https://github.com/user-attachments/assets/f794f734-39af-4192-a0b4-30c1d6b52166" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="1191" alt="432242530-d41f22f0-20dc-4fc5-969a-c6cfc42b7a6e" src="https://github.com/user-attachments/assets/a24ada25-7050-4517-826a-8663ee319655" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1191" alt="432242558-cb089d7e-ae48-4d2e-897a-ad7b1cec56b5" src="https://github.com/user-attachments/assets/dc11c28e-244e-454b-b12a-14423040dd2b" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1191" alt="432242600-5b41966d-aae6-403b-b636-8a59c5195918" src="https://github.com/user-attachments/assets/f3670891-3b75-4e1a-aa04-0d82e922719d" />


seq 10 
## OUTPUT

<img width="1191" alt="432242629-d2d79471-6bde-4777-9657-136e0f248791" src="https://github.com/user-attachments/assets/e0e02687-d1c7-4dcd-83d3-7ba7b0b00c64" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1191" alt="432242671-846623a8-eedd-4b94-a610-680c6178279b" src="https://github.com/user-attachments/assets/90244802-ad97-47ee-9a94-36ccb5db1c65" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1191" alt="432242710-576c416c-6a8d-49b8-a403-94928e39e8e2" src="https://github.com/user-attachments/assets/3f4a9554-e76b-4007-be25-07362b8ffe2b" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="1191" alt="432242736-a0d1d2a0-8ee5-48f8-a26c-01837f8bf504" src="https://github.com/user-attachments/assets/576ee041-45c0-4640-9ec3-95a363858866" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="1191" alt="432242790-4136f92e-76f1-482b-8c1b-98bacd52a44b" src="https://github.com/user-attachments/assets/0bbbe750-818c-4eba-8ba7-3b8c8bfd07f7" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1191" alt="432242818-7572a7c5-b120-404a-944a-a0fb44a34c39" src="https://github.com/user-attachments/assets/4d0b7ea0-e393-44eb-9f28-41775e9bf520" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1191" alt="432242954-fee93d2b-e820-405d-829c-cb3ac77d6913" src="https://github.com/user-attachments/assets/ee945479-0798-4417-8ff4-f6e1b4503975" />


sed -n '2,4{s/$/*/;p}' file23
<img width="1191" alt="432243028-d315d25b-0171-4c89-bf27-598b2ce1de6e" src="https://github.com/user-attachments/assets/02311cab-6302-4ac2-9870-51ae202c23b6" />


#Sorting File content
cat > file21

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
sort file21
## OUTPUT
<img width="1191" alt="432243126-5333cc08-329e-4da2-8233-3095e90b7d7a" src="https://github.com/user-attachments/assets/d3f4c0b7-315c-4343-be3c-12a26a4dc550" />


cat > file22

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
uniq file22
## OUTPUT

<img width="1191" alt="432243157-245bb0b0-0255-4f81-8d8b-c4d29b50d05a" src="https://github.com/user-attachments/assets/a224a32e-1120-4ea7-ba64-10bb1c1e2d32" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1220" alt="432243200-b0085bbf-9a45-402f-b14c-ece48e2602fe" src="https://github.com/user-attachments/assets/441a2585-8ae9-4471-ad88-0be876129b64" />

cat < urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
^d
 
cat > urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
 
cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="1150" alt="432243264-e03f12ce-785a-45ef-9624-4563248f0b34" src="https://github.com/user-attachments/assets/c7ba5b39-d880-4366-b61e-2ddb7a5c80c6" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1262" alt="432243332-ccc45ef6-7b2e-49e5-bb75-ebbac286edd5" src="https://github.com/user-attachments/assets/59a25bbb-08d6-4810-9dea-a3f7094a2342" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="983" alt="432243358-7dda13ca-4234-4c36-a5c9-adb5ec42b766" src="https://github.com/user-attachments/assets/58448834-8384-4a01-a710-2f7921598f94" />


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="983" alt="432243567-6b40597b-d048-42ce-934a-818b56688bce" src="https://github.com/user-attachments/assets/86174994-90f9-440d-938b-03fdbd2a1c06" />


tar -xvf backup.tar
## OUTPUT
<img width="983" alt="432243624-fe693983-4dbf-4cdf-8152-65628495ab33" src="https://github.com/user-attachments/assets/727637a1-87c3-4d24-bc73-9de229968267" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="983" alt="432243663-876904f8-34e8-4580-b53a-ffeb3af31649" src="https://github.com/user-attachments/assets/870a9f40-e981-4c18-aea9-b19b19b2db1c" />

gunzip backup.tar.gz
## OUTPUT
<img width="1112" alt="432243720-aa3cc13c-ba98-4aeb-939f-a4606374ff64" src="https://github.com/user-attachments/assets/b6d8e172-9275-4bbb-915b-11546e3cda25" />

 
# Shell Script

echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh

chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1303" alt="432243768-326b813b-3add-459f-b2fd-338b43528e77" src="https://github.com/user-attachments/assets/aa8640e3-43f2-47a0-a716-9e97e3f78582" />

 
cat << stop > herecheck.txt

hello in this world
i cant stop
for this non stop movement
stop


cat herecheck.txt
## OUTPUT
<img width="1303" alt="432243797-5c12b41c-eee4-4d2e-8349-cf8bb6a94019" src="https://github.com/user-attachments/assets/cb2586c0-561d-49c3-952d-14357e1d852b" />


cat < scriptest.sh 
bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " basename $0
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 

cat scriptest.sh 
bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " basename $0
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps

 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 <img width="1303" alt="432243806-a1d01a1b-620c-49f0-af5c-b40f49969e3e" src="https://github.com/user-attachments/assets/ad960d06-7b36-44fd-b848-1f7f0fc15c35" />

ls file1
## OUTPUT
<img width="1303" alt="432243838-91dbf86e-7838-4f5a-b9eb-1e397b632533" src="https://github.com/user-attachments/assets/463bf8e8-3a70-4c94-a8cb-ca3be64149b2" />

echo $?
## OUTPUT 
<img width="1303" alt="432244042-1feae372-1cc6-402a-9c5c-f3be43581725" src="https://github.com/user-attachments/assets/8ac82f93-59d6-47e9-a767-47594b761eb7" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="1303" alt="432244078-3386c71f-9b56-4054-8d20-c32b458ff88a" src="https://github.com/user-attachments/assets/62a34dad-9963-4898-a74b-d10fb7117f89" />

abcd
 
echo $?
 ## OUTPUT

<img width="1303" alt="432244111-b3c78bca-e8d4-467d-87fe-0413e4ae6b9c" src="https://github.com/user-attachments/assets/2d340b48-6dd8-49a6-9a49-70200384f9a6" />

 
# mis-using string comparisons

cat < strcomp.sh 
bash
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


cat strcomp.sh 
bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi

##OUTPUT


<img width="1303" alt="432244155-ef3087fe-ada2-4949-8add-8535c550bbfb" src="https://github.com/user-attachments/assets/88ab1775-3622-4fa9-b105-51eb0b1ef928" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1303" alt="432244206-c90593e2-4593-47b0-a659-84b7b0694bfa" src="https://github.com/user-attachments/assets/a9a94c63-e380-4180-a0fd-06f6481a50b1" />


# check file ownership
cat < psswdperm.sh 
bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d


cat psswdperm.sh 
bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 
./psswdperm.sh
## OUTPUT
<img width="1303" alt="432244238-0a51caa3-16be-4d68-99cb-0e6f1a0dd884" src="https://github.com/user-attachments/assets/979642bf-ab84-408d-aee4-afec8ed66911" />

# check if with file location
cat>ifnested.sh 
bash
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

cat ifnested.sh 

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


./ifnested.sh 
## OUTPUT
<img width="1303" alt="432244265-3da26632-b35a-4002-badf-4eb936d859fc" src="https://github.com/user-attachments/assets/0221ba33-3941-4334-8d45-8c952100019a" />



# using numeric test comparisons
cat > iftest.sh 
bash
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



cat iftest.sh 
bash
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


$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
<img width="1303" alt="432244414-d3707e4f-5b05-4165-b7c4-54d71467dbe3" src="https://github.com/user-attachments/assets/33123716-2b09-4534-99a7-53b2d4361d79" />

# check if a file
cat > ifnested.sh 
bash
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


cat ifnested.sh 
bash
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


$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
<img width="1303" alt="432244667-03b3d541-ae43-49fe-a679-b8bf018815f1" src="https://github.com/user-attachments/assets/5399b2f5-ca1d-41e8-a8a9-a439d3c5fd2a" />

# looking for a possible value using elif
cat elifcheck.sh 
bash
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


$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
<img width="1303" alt="432244790-b1919683-5d80-4cbb-8c3a-01a1e6ea0afa" src="https://github.com/user-attachments/assets/abd18dc3-d368-4e01-9e99-2af297cc0ba2" />


# testing compound comparisons
cat> ifcompound.sh 
bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi

$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="1303" alt="432244869-9bc65215-3ed3-443c-9bf8-59c2fea04b30" src="https://github.com/user-attachments/assets/6bb3894d-0549-4915-aeb2-86831d283529" />

# using the case command
cat >casecheck.sh 
bash
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

$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 <img width="1303" alt="432245050-de882c6a-f548-4fbe-8eb7-f3e11aa3f7a4" src="https://github.com/user-attachments/assets/0c1967b1-745a-4d4a-8f90-28bb9753c055" />

cat > whiletest
bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done

$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 <img width="1303" alt="432245096-46ef979e-69bf-4c0b-b3c2-d4c696605c94" src="https://github.com/user-attachments/assets/69e1e1fb-d776-40fe-8bea-a75262c3836d" />

 
cat untiltest.sh 
bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
 
$ chmod 755 untiltest.sh
 <img width="1303" alt="432245145-3f62dc3a-31bb-4eb0-a6c7-8529d13fce33" src="https://github.com/user-attachments/assets/423256c4-d738-45d2-be54-2232323d7db4" />

 
 
cat forin1.sh 
bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 
 
$ chmod 755 forin1.sh
 <img width="1303" alt="432245174-a888656f-4867-4a46-9750-3b4272408f5b" src="https://github.com/user-attachments/assets/a8f65cf8-dd0f-4337-80f1-8e734bd998b0" />

 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 
 
$ chmod 755 forin2.sh
 <img width="1303" alt="432245955-7bb432e5-d9ee-4599-bf13-5438cc5f4e6e" src="https://github.com/user-attachments/assets/782b240d-9c7b-410e-9a9e-59f3d555e0c2" />

cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done

$ chmod 755 forin2.sh
 

$ ./forin2.sh 
 <img width="1303" alt="432246001-237ad428-e9b7-4ac3-821e-3da854d3074d" src="https://github.com/user-attachments/assets/ca34bb6e-0ca5-44e9-916e-a734ebd063f0" />

cat forin3.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done

$ ./forin3.sh 
 <img width="1303" alt="432246159-13b0597a-c4e7-4911-bc4b-aacde0ab3821" src="https://github.com/user-attachments/assets/9d96b4fa-88ca-4412-b191-46b119538787" />

cat forin1.sh 
bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done

$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
bash
#!/bin/bash
# reading values from a file
file="cities"
for state in cat $file
do
echo "Visit beautiful $file“
done

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
bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
`
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
<img width="1303" alt="432248217-d025e8ab-8914-4773-b7b8-20af63ecd3a2" src="https://github.com/user-attachments/assets/46a2d3ab-40a0-40fb-8b70-505106f9d872" />

cat forctype1.sh 
bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done

$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
<img width="1303" alt="432248176-4f1d5d1c-9596-47ef-9846-241cfbf36477" src="https://github.com/user-attachments/assets/2d3404bd-93d1-4825-a108-bf1e682291ef" />

cat fornested1.sh 
bash
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

$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
<img width="1303" alt="432247930-5dab4256-25ff-4602-a718-93d078bc5b83" src="https://github.com/user-attachments/assets/dbb8e455-a49d-4ca7-86de-7d19519053df" />

 
cat forbreak.sh 
bash
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

## OUTPUT
<img width="1303" alt="432247452-2c3004a2-8341-49fe-99d2-7d733e2d738f" src="https://github.com/user-attachments/assets/34bc5dcf-135f-4f16-8f32-8ff21b303547" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
bash
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


 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 <img width="1303" alt="432247452-2c3004a2-8341-49fe-99d2-7d733e2d738f" src="https://github.com/user-attachments/assets/b2393853-c673-4005-be17-3ba45cd04841" />

cat exread.sh 
bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
<img width="1303" alt="432247397-67e32e61-c7fe-41e2-8a25-6d7f5083b7e4" src="https://github.com/user-attachments/assets/b6d38cf2-b779-4339-9893-7098dee50fb8" />


 cat exread1.sh
bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="1303" alt="432247283-54d08463-e8d4-44e0-a8b5-fe2769e83721" src="https://github.com/user-attachments/assets/e3cb8577-ee64-434b-bfac-beb2b0588f0b" />


$ ./exread1.sh 
 
cat funcex.sh
bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=func $1 $2
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi

## OUTPUT
 ./funcex.sh 

 <img width="1303" alt="432246863-40654afd-9dbe-402d-8eee-49993bd05766" src="https://github.com/user-attachments/assets/6ba7beaf-1c1c-4a08-961e-ab62965238b9" />

 ./funcex.sh 1 2
<img width="1303" alt="432246883-36b0ca02-3fff-4225-b684-e0f9cba56ec4" src="https://github.com/user-attachments/assets/4ba4a954-9e35-4511-9d16-2c8e6bc4c15b" />

 
cat argshift.sh
bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done

$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 <img width="1303" alt="432246811-6ab174df-28db-4227-a7c0-437897d6c105" src="https://github.com/user-attachments/assets/10fdc7e3-85c9-4f96-b7be-f69b31f16076" />

 cat argshift1.sh
bash
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

$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 <img width="1303" alt="432246575-68844e48-a0f0-4f21-8755-f08681b35ebe" src="https://github.com/user-attachments/assets/9af3af3d-32b0-49b8-9331-12e71e4c9a70" />

cat argshift.sh
bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x

## OUTPUT
 ./argshift.sh 1 2 3
 
 <img width="1303" alt="432246474-0c1a0221-6aa6-4d54-a7bf-f1dd413f5f54" src="https://github.com/user-attachments/assets/824ff09c-ec54-4111-814c-80d061a3d458" />

cat > nc.awk
bash
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
 
cat>data.dat
bash
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

awk -f nc.awk data.dat
## OUTPUT 
 <img width="1303" alt="432246407-ae636339-1207-4ec2-8669-e590f9fad49c" src="https://github.com/user-attachments/assets/7313c94b-bdb1-4b4f-9f11-a3dbb99afa46" />

cat > palindrome.sh
bash
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

## OUTPUT 
<img width="1303" alt="432246358-b32df0c4-a18c-4a9e-81f7-d3036a27a88e" src="https://github.com/user-attachments/assets/7c87ec0b-2023-4bd0-934c-bb2eae4e6dfa" />


# RESULT:
The Commands are executed successfully.
