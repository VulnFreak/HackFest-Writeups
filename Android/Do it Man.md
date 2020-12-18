# Do it Man

`Not To Hard Just Do It and Show your All Rounder `

`Hint - Use the command "apktool".`

Firstly, we are given the application chall.apk file. 
1. We will now use `apktool d chall.apk` [Here d is used to decompress the apk file]
2. We have now obtained a file named : chall
3. cd chall
4. ls
5. We now have the files present in the folder : AndroidManifest.xml ; apktool.yml ; original ; res ; smali ; smali_classes2
6. We use the command : grep -rn "hf0x01" *
7. We can now see that we have obtained the flag in "smali_classes2/com/hackers/doitman/MainActivity$get_flag.smali"

The output should be : smali_classes2/com/hackers/doitman/MainActivity$get_flag.smali:34:    const-string v0, "hf0x01{Y0u_4r3_n0w_B4s1c_4ndr01d}"

Flag : `hf0x01{Y0u_4r3_n0w_B4s1c_4ndr01d}`
