# Goldman Sachs Forage Job Simulation

## Table of Contents

- [Memo](#memo)
- [Requirements](#requirements)
- [Usage](#usage)
- [Results](#results)
- [Author](#author)
- [Certificate](#certificate)

**Subject**: Assessment of Password Policy and Recommendations for Improvement

## Memo

```txt
Dear Sir/Ma'am,

I used https://crackstation.net/ to quickly crack 13 passwords out of the 19 hashcodes provided in the password dump file. 

I tried to decipher all of the stolen hashes and discovered a few weaknesses in your password policy. This email summarizes my findings and offers recommendations for strengthening your password policy. 

For data security during authentication, the two most used cryptographic hash algorithms are Secure Hash Algorithm (SHA) and Message Digest (MD5). Every password that was hacked used MD5, a hash method that is less reliable and more likely to cause collisions. 

Using the wordlists from rockyou.txt and hashcat.com, it was relatively simple to crack using a web browser and a terminal. To generate hashes for the passwords, I would advise using an extremely strong password encryption method.

After cracking the passwords, I found the following things about the organization’s password policy: 

· Minimum length for a password is set to 6. 

· There is no specific requirement for the password creation. Users can use any combination of words and letters to create a password. You can include several new things in your password policy. 

My recommendations are: 

· Avoid common words and character combinations in your password. 

· The longer passwords are better, 8 characters is a starting point. 

· Don’t reuse your passwords. 

· Include special characters, Capital and Small letters, and numbers in your password. 

· Don’t let users include their username, actual name, date of birth, and other personal information while creating a password. 

· Train your users to follow these policies to keep their passwords safe.


SECURITY ALGORITHMS USED WITH 13 CRACKED PASSWORDS

e10adc3949ba59abbe56e057f20f883e          md5 - 123456

25f9e794323b453885f5181f1b624d0b          md5 - 123456789

d8578edf8458ce06fbc5bb76a58c5ca4          md5 - qwerty

5f4dcc3b5aa765d61d8327deb882cf99          md5 - password

96e79218965eb72c92a549dd5a330112          md5 - 111111

25d55ad283aa400af464c76d713c07ad          md5 - 12345678

e99a18c428cb38d5f260853678922e03          md5 - abc123

fcea920f7412b5da7be0cf42b8c93759          md5 - 1234567

7c6a180b36896a0a8c02787eeafb0e4c          md5 - password1

6c569aabbf7775ef8fc570e228c16b98          md5 - password!

3f230640b78d7e71ac5514e57935eb69          md5 - qazxsw

917eb5e9d6d6bca820922a0c6f7cc28b          md5 - Pa$$word1

f6a0cb102c62879d397b12b62c092c06          md5 - bluered

16ced47d3fc931483e24933665cded6d          md5 

1f5c5683982d7c3814d4d9e6d749b21e          md5 

8d763385e0476ae208f21bc63956f748          md5 

defebde7b6ab6f24d5824682a16c3ae4          md5  

bdda5f03128bcbdfa78d8934529048cf          md5 

9b3b269ad0a208090309f091b3aba9db          md5 


Observations

1)What type of hashing algorithm was used to protect passwords?

Ans: Md5


2)What level of protection does the mechanism offer for passwords?

Ans:  MD5 is insecure and provides a very low level of protection and should not be used in any application.


3)What controls could be implemented to make cracking much harder for the hacker in the event of a password database leaking again?

Ans: Controls to be implemented to make cracking harder:

i) A minimum length password rule should be implemented.

ii) Passwords must contain some special characters, numbers, lowercase alphabets as well as upper case alphabets. 

iii) Using a hashing algorithm that provides a high level of protection. Example: SHA-256 and SHA-3.

iv) The concept of password salting must be used.


4)What can you tell about the organization’s password policy (e.g. password length, key space, etc.)?

Ans: i)There is no rule regarding the minimum length of the password.

     ii)There is no rule regarding the use of special characters in the password.


5)What would you change in the password policy to make breaking the passwords harder?

Ans: i) The password must be of minimum 8 characters.

ii) Minimum 2 special characters (/,#,*,... etc)  must be used in the password.

iii)An external Api-based tool that checks for password strength should show that the used password is strong.


I appreciate your consideration of these findings and recommendations, and I look forward to collaborating with you to further bolster our security measures. Should you require any additional information or clarification, please do not hesitate to reach out.

Sincerely,

Ohinoyi
Texas Tech University '27
```

## Requirements

- [Hashcat](https://hashcat.net/hashcat/)
- [Rockyou.txt](https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt)

## Usage

```bash
hashcat -m 0 -a 0 -o decrypted.txt hashes.txt rockyou.txt # to crack pass
hashcat -m 0 -a 0 -o decrypted.txt hashes.txt rockyou.txt --show # to see it again after 1st time decryption
```

## Results

```sh
Security Algorithms used(listed below): 

experthead:e10adc3949ba59abbe56e057f20f883e – MD5
interestec:25f9e794323b453885f5181f1b624d0b – MD5
ortspoon:d8578edf8458ce06fbc5bb76a58c5ca4 –MD5
reallychel:5f4dcc3b5aa765d61d8327deb882cf99 –MD5
simmson56:96e79218965eb72c92a549dd5a330112 – MD5
bookma:25d55ad283aa400af464c76d713c07ad – MD5 
popularkiya7:e99a18c428cb38d5f260853678922e03 – MD5
eatingcake1994:fcea920f7412b5da7be0cf42b8c93759 – MD5 
heroanhart:7c6a180b36896a0a8c02787eeafb0e4c – MD5
edi_tesla89:6c569aabbf7775ef8fc570e228c16b98 – MD5
liveltekah:3f230640b78d7e71ac5514e57935eb69 – MD5
blikimore:917eb5e9d6d6bca820922a0c6f7cc28b – MD5
johnwick007:f6a0cb102c62879d397b12b62c092c06 – MD5
flamesbria2001:9b3b269ad0a208090309f091b3aba9db – MD5
oranolio:16ced47d3fc931483e24933665cded6d - MD5
spuffyffet:1f5c5683982d7c3814d4d9e6d749b21e - MD5
moodie:8d763385e0476ae208f21bc63956f748 - MD5
nabox:defebde7b6ab6f24d5824682a16c3ae4 - MD5
bandalls:bdda5f03128bcbdfa78d8934529048cf - MD5

Cracked Passwords(listed below):

experthead:e10adc3949ba59abbe56e057f20f883e - 123456
interestec:25f9e794323b453885f5181f1b624d0b - 123456789
ortspoon:d8578edf8458ce06fbc5bb76a58c5ca4 - qwerty
reallychel:5f4dcc3b5aa765d61d8327deb882cf99 - password
simmson56:96e79218965eb72c92a549dd5a330112 - 111111
bookma:25d55ad283aa400af464c76d713c07ad - 12345678
popularkiya7:e99a18c428cb38d5f260853678922e03 - abc123
eatingcake1994:fcea920f7412b5da7be0cf42b8c93759 - 1234567
heroanhart:7c6a180b36896a0a8c02787eeafb0e4c - password1
edi_tesla89:6c569aabbf7775ef8fc570e228c16b98 - password!
liveltekah:3f230640b78d7e71ac5514e57935eb69 - qazxsw
blikimore:917eb5e9d6d6bca820922a0c6f7cc28b - Pa$$word1
johnwick007:f6a0cb102c62879d397b12b62c092c06 - bluered
```

## Author

- [Ohi](https://github.com/Ohimoiza1205)

## Certificate

[image](https://github.com/user-attachments/files/16323178/Goldman-Sachs-SWE.pdf)

