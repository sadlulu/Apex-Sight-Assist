# Apex
**Apex legend assist**
\
\
Made by Stone Luo
\
\
Credit to [@TheCruZ](https://www.unknowncheats.me/forum/members/1117395.html) for original EFI source code.
\
\
***There is a GPL 3.0 License, so DO NOT do illegal things like selling it!!!***
\
\
**[Video Showcase](https://youtu.be/u4Dmnn4py4g)**
\
\
Compatible with: *Steam and Origin*
\
\
**Usage**
\
\
Bold enemy if they are close by to help people see better (think of it as crypto's drone release check)

Visual Check checks if enemy is in sight
```
//store this somewhere globally:
float visiblePlayerInfo[75] = {};
 
 
//do this to know if visible or not:
bool visible = false;
float LastVisibleTime = 0.f;
read<float>(entity + OFFSET_LAST_VISIBLE_TIME, &LastVisibleTime);
 
visible = LastVisibleTime > 0.f && LastVisibleTime > visiblePlayerInfo[index];
visiblePlayerInfo[index] = LastVisibleTime;
```

Change color spectrum for difference enemies, according to the enemy's shield level

Teammate exception: teammates are labelled in special color, so player can avoid shooting at teammates and bullets getting blocked

Aim assist: tracks enemy with movement and bullet travel prediction.(based on enemy's movement when the bullet is shot, also keeps track of bullet projectile)

Spectator count: tells how many people are spectating you even in rank
\
\
**Help Me Improve**
\
\
Interested in making this a better program? Contact me!\
Email contact: stoneluo.steam@gmail.com
\
\
**Instructions**

1. download the release and compile code to get the EFI mapper

2. find an injector yourself, whether it's interception or extreme, whatever

3. put the efi driver into a usb drive(must be formatted to FAT32)

4. restart the computer and choose to boot with the usb drive\
follow these steps

```
FS0:
load memory.efi
FS1:
1. ls (check if there's efi and boot file)
> if no
fs3: -> check, fs3: ->check, etc
> if you found it
cd efi
2. ls (check if there's Microsoft)
> if no
back to step 1
> yes
cd Microsoft
look for mgftwboot.efi and type it in the shell
```

5. you should boot normally into windows if you did everything properly

6. open an application such as notepad and inject the release dll

7. enjoy your game!

\
\
**Change logs**
\
\
Release 1: season 7 offset updated

Improved aim assist
\
\
\
Release 2: season 8 offset updated

EAC got updated, they seem to detect it. DO NOT USE for now.
