# School Assistant

`Our school want to help the students to manage their daily schedule therefore we made a school assistant apk but after sometime we get notifed by students that 
google play store protect blocking the apk and it also taking extra permission like camera, file storage, microphone but this permission are not intended and 
we also recieved complain that sometime camera opens on their own. So we have the apk which students have and you have to find which organisation is behind this. `

`Hint - Use the command "apktool" and "grep".`

Firstly, we are given the application School_assistant.apk file. 
1. We will now use `apktool d School_assistant.apk` [Here d is used to decompress the apk file]
2. We have now obtained a file named : School_assistant
3. `cd School_assistant`
4. `ls`
5. We now have the files present in the folder : AndroidManifest.xml | apktool.yml | assets | kotlin | original | res | smali | smali_classes2 | unknown
6. We use the command : `grep -rn "hf0x01" *`
7. The output is : 'Binary file original/META-INF/ALIAS_NA.RSA matches'
8. `cd original/META-INF`
9. Using a text editor : `gedit ALIAS_NA.RSA` we obtain the required flag

The output is : hf0x01{w3_w1ll_b3_shutd0w1ng_C0mpl3t3_N3twork$_by_Tomorrow}10UUnknown10UMr Robot0

Flag : `hf0x01{w3_w1ll_b3_shutd0w1ng_C0mpl3t3_N3twork$_by_Tomorrow}`
