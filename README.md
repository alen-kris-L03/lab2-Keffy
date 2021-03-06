# Lab 2: Gene Exploration on Amazon Web Services

# Part I: Get Set up on AWS

  Part I is adapted from [http://jnmaloof.github.io/BIS180L_web/2019/04/02/0AWS_Setup/](http://jnmaloof.github.io/BIS180L_web/2019/04/02/0AWS_Setup/)
(You may also look there, if you like).
Note: some of the images used here are from an older version of AWS Educate.

  Most bioinformatics software runs on Linux or unix (including Mac) operating systems. For this class we will work in a Linux environment. Since the computer lab machines run Windows this presents a problem. To overcome this problem we will run Linux in a virtual cloud environment. [What is Linux?](https://www.linux.com/what-is-linux)

Specifically we will use [Amazon Web Services (AWS)](https://aws.amazon.com/). AWS is a cloud computing resource provider. We will run virtual Linux machines on AWS servers and then use a [virtual network connection (VNC)](https://en.wikipedia.org/wiki/Virtual_Network_Computing) to display the “desktop” of the virtual machine to be displayed on our local computer, or by connecting through a text-based terminal.

AWS is not free, but as a student in this class you get a $100 credit. $100 should be enough credit for you to complete this class so long as you suspend your instance when not in use. For example a 2 cpu, 8GB instance costs $0.093 per hour. In addition, you will need to pay for storage.

It is possible to connect to your AWS instance from computers anywhere in the world.

## Creating an AWS account

This section is not technically necessary, but if you plan to use AWS in the future it is recommended as it will allow you to receive $100 in service credit each year until you graduate. If you choose to not create an AWS account, proceed to the “Creating an AWS Educate account” section of this guide.  
Note: In order to complete these steps, you will need to have a valid credit card

1.  Go to [AWS.amazon.com](https://aws.amazon.com/)
    
2.  Click Create an AWS Account
    
3.  If you have an amazon account login with your amazon credentials (If not, create an account)
    

-   Follow the instructions to create your account.
    
-   On the Contact Information page select Personal Account
    
-   For Support plan, the free option has already been picked, just click continue
    
5.  If the instructions have been followed, your AWS Account should be created.
    

## Creating an AWS Educate account

__ You need to do this even if you created an AWS account above__

1.  By now you should have already received an email invitation from AWS Educate Support with the subject “Your AWS Educate Application”![AWS_Educate](https://lh4.googleusercontent.com/SBFifSB6G2Ww9h8u7H-KUQZAqOUh8543K8JqJqb82bv81KOoGpFLApnzryKZNYp1ERYui8DjRkEO7i4_L_xRym_T6uQuG5jhmawqpnmrm0L0fD6-dvmr_Sr6Mbld_TDeKOtHdzH1)Click on the blue link “here” to continue to the next page. Fill out the appropriate information
    
2.  Fill out the form appropriately![AWS_Educate](https://lh4.googleusercontent.com/H1X8WBorQF8EnkkXEK1g9e8BWBWYlPnbN-WW1klLT1NfsYAWPNU2KtjyqCQnJxbpgbsgSJ3gA2tJbEegpNViq8Ll9jk66k2cg2XpzIhRhs-Ow_x_9PdhbjY1tXk22P8_HQVB8WOR)
    
3.  If you created an AWS account, input your AWS Account ID. Otherwise select AWS Educate Starter Account
    

-   Your AWS Account ID can be found at [https://console.aws.amazon.com/billing/home?#/account](https://console.aws.amazon.com/billing/home?#/account)
    

5.  Complete the verification process
    
6.  Your application should be approved within 1 minute and you will receive an approval email if you followed the steps correctly.![Approved_Message](https://lh3.googleusercontent.com/TK_SkA0QigMMfKbZSKpRwE6RI11Ms-3Qt3OX84euFa_IeTExSR9OsUawp_BV3XcFFXI62oqyjKd1aeUXZJ5NtP31u3j7jrdRebsPuSAsmkRPSNZFYibABZ9EotvgLcXypLXU4oH1)
    
7.  Click on the link in the email to set your password
    

## Entering the classroom

1.  Navigate [AWS Educate](https://aws.amazon.com/education/awseducate/) and login![AWS Educate Homepage](https://lh6.googleusercontent.com/6MoBbmeGmiAokwLKKcfe_8jkpP8mArQaAKGcbTeRayr22AnE2wu3JrM9ufZu-A14rJMMYl-LqVkh3xahNULbbgt1m-rz6F3AbIeHwcqqSa0m_mR0o_pNlgLJ_qgXGjprfxmdBsks)
    
2.  Click on My Classrooms tab![AWS Homepage](https://lh5.googleusercontent.com/J-elj7XMmA_hw695p3BOfyqUT6tE4Fq9ksVBIs7CkQJSg792qMjrsfqRK-PmskPB-nVxdTqUVWxiQHf59tmpA69JviVQC6CrJljsSL3XHw8Jzhq8fhWk7uRCoSRIOS3S6bwIaQo5)
    
3.  Select the Bio 312 classroom
    
4.  Enter the AWS Console![Classroom](https://lh6.googleusercontent.com/G8y3WANRe-yETYdsTd6ZOx69arlctAy0PJuYhvr3fM5JG10hL7wTtfGgP2bgwCmVkecuDHrh_PJZU15V45MVwzIBVgK3eITWgEZ8hE9ZX0eqi7SVOlK3fjxJVl5wHYg22yhRCW8b)
    
5.  Navigate to the EC2 Service![EC2 Select](https://lh4.googleusercontent.com/YqiZf3g9qkFT99QP18CKazkT8y9kiOHSlxxkTy6wjU0dOuNXlN5WzEedVBswTmXDvj8knqao3MFGLUF5EbIUDxOUCoqjqvzJIir_Gtp0BJ9nAwpAg3noJEB8gQuI_WeqLSxy293E)
    

Since we are working inside the AWS classroom environment, we do not have access to everything AWS has to offer. Look at the upper, right portion of your window, you will see it says “N. Virginia”

## Creating your BIO312 instance

An instance is your realized virtual machine. It is an instance of a machine image that defines the programs, files, and operating system.

 1.  Go to [your ec2 console](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1)
    
 2.  Click on the blue button in the middle of the screen saying “Launch Instance”
      ![EC2_Home](https://lh6.googleusercontent.com/i-W-YAkMphD068LJYOETtrhdjuCb1dOCRL-px9wlR-tW8ZmGJoZDNPSDM3_1ifW2dAR1Vgt2EewVttJMXLIW9e9FwViFSEb8GCboED_eQZSdGGVoKmbQD5IAuE4YQ5X72frCmyMm)
    

 4.  Click on **Community AMIs** in the menu on the left
    
 5.  In the search bar search for BIO312
    
 6.  Select **Bio312-2021 ami-0baa78a354f6c7570**
    
 7.  On next page select t2.medium. ![EC2_Instance](https://lh6.googleusercontent.com/qvGMXf_B0_2JfHlsf-qM86_-uo8l7l04R5jhrFcbIk-bprtewSx1sQajklnuVcn16dQSWkQVWyoiIuJss6_ZKoIChVZLfPDplGx8mOXzcegrFdTd2J4hEByahS4VFTu00Y6uXoth)
    
 8. For storage, choose the default 50GB.    
 9.  Click “Configure instance details”. Under "Security Group" make sure “create a new security group” is selected.  **SSH ** should be displayed. **Also add  another rule ("Add Rule"), and then select **HTTP****.

![EC2_Security](https://lh6.googleusercontent.com/4Gklw-G_W1DmHID1B5z-wHUPdSmPpQGbJ3VKoZE1rXLm7BlvOzpNqZyEXQ_Zl3JVVm3NSDxo9jbijtoQBvtbK9RB0d_fKX97C1vp6PBVIoOEjFfRUo_FKtH-h-7SsmbALc2IyVXI)
    
11.  Click Review and launch at the bottom of the page
    
12.  Click Launch
    
13.  Select “Create a new key pair”![EC2_Key](https://lh3.googleusercontent.com/womxrtLufSZgrBQmjimFbRU5F4uHQD41pAcpc2i7zcYKZYvsxjo1QfJcJc9rWITTaQXqVdgfQ2Gl4Bd8tHelQ8Hv8W88H0aJbG5IeVVK9x2Ve8g61_7TwAU9Yiz_xXW8xE8ozKY-)
    

-   Name it whatever you want
    
-   Click the Download button
    
-   Press “Launch Instance”
    
-   Email the *.pem file to yourself, in case you need it in the future. (This is not a secure practice, however presumably you won’t be storing anything sensitive on your instance)
    
-   Click “View instance” on the lower left hand corechner
    
  

  **NOTE: on a mac, you need to change the permissions of your pem file. (replace /path/to/your.pem with your own info):**  
  

    chmod 0400 /path/to/your.pem
    

>    [GitHub]: What is the path to and name of your .pem file on your
> computer? Write it here:

   
On the PC, if you move your file to the same directory as your command prompt, this should solve the permissions issue.

## Attaching Permanent IP address to instance

[Internet Protocol (IP) addresses](https://en.wikipedia.org/wiki/IP_address) are used to connect to various resources on the internet. We want to assign a permanent IP address to your instance so that you know where to find it.

1.  Go to [AWS Elastic IPs](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#Addresses:sort=PublicIp) (scroll down on the left hand menu until you see this).![EC2_Elastic](https://lh4.googleusercontent.com/KNPah00lM1OpfPNhFh1c3iGnfvZRljcrCQCEuLMW2hXwiO-_IMQzBBnc-UUPL2_oFcganCzzr4ZH5v72YSnhe7KNH6TPjhY2PbuJm2Qkep3u3Vt3JerTRcJSqImivHtMcYUohVgy)
    
2.  Click “Allocate New Address”
    
3.  Choose “AWS pool”
    
4.  Click on “Actions” followed by “Associate Address”
    
5.  On the pop-up window click on the instance box and the name of your instance will pop up, click on it followed by “Associate” at the bottom of the window![EC2_Associate](https://lh3.googleusercontent.com/3tnipsgidWFh377TWIvlMwmB8v-S0FRmww96vdae74rUjglE_TPjw1uHRYazVDgKyMRVQMgs94iPCuaFXH-PqaPvGFybD0QuaNKBrVixk--8JkjXoLkXep0FD6bnMcQe55ZBqL_t)Save this IP address. Write it down, or perhaps email it to yourself. You can also find it on your AWS console anytime that you need it.

>  [GitHub]: write your elastic IP address here:

 

## Connecting to your Instance via SSH

Connect using a [secure shell(ssh)](https://en.wikipedia.org/wiki/Secure_Shell) text connection. This allows you to send and receive text from your virtual machine’s linux “console”. A SSH connection is a good choice if your network connection is slow or if you don’t need any graphical display. This is the standard way to connect to a Linux server for many people. It is much better when the network is slow. For most labs, only an ssh connection is necessary.

**On a PC running windows 10, a mac, or chromebook, find the terminal or command prompt**. Using spotlight or the magnifying glass, search for "terminal". On the mac, launch terminal. **If you are on a Windows machine, try typing "ssh" to see whether this is installed. If not, consider installing the Windows Subsytem for Linux (google this).**

Here's how to connect form the command prompt:
Your username is ec2-user. Your IP address is elastic IP assigned above. Type the following into the terminal:

[If you haven't already, be sure to change your permissions:

    chmod 0400 /path/to/your.pem
or put it they key pair in the default command prompt directory: 

    C:\Users\XXXX
where XXX is your username.]


ssh -i my.pem ec2-user@52.53.117.125

Replace the “52.53.117.125” with the IP address of your instance.

Replace my.pem with the name of your .pem file, including its path/directory (or use cd to change directory to your current location.)



### IF YOU COULDN'T CONNECT FROM YOUR TERMINAL OR COMMAND PROMPT - you can use PuTTY - on a Windows PC without a linux terminal (if the above worked for you - skip this section).
Install Putty from https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
You will probably select the following installer:
[`putty-64bit-0.74-installer.msi`](https://the.earth.li/~sgtatham/putty/latest/w64/putty-64bit-0.74-installer.msi)

#### Convert Your Private Key Using PuTTYgen

1.  When you installed Putty, it came with Puttygen. There is a one time step to convert your .pem security key. Start PuTTYgen (for example, from the Start menu, choose All Programs > PuTTY > PuTTYgen).
    
2.  Under Type of key to generate, choose RSA. ![puttygen-key-type](https://lh5.googleusercontent.com/tPCmr0xQtxgWEq2hMTwWvDKZGSeRl8ErV5nwFRQHZuLDcID7VAAYDV0pfOoGSMg7H_8r0BrsSEjnDbpmavjYc1ei05k0uGAlUZ3Qxcd7sKrFMKYbIlUzHztQ37QAOwv9_d-thX7j)
    

3.  Choose Load. By default, PuTTYgen displays only files with the extension .ppk. To locate your .pem file, select the option to display files of all files types. ![puttygen-load-key](https://lh6.googleusercontent.com/iXqzSi9ETZSTIIWWY3037A8I81ISUpm6F8LOaIQr_qiUMkB5XF8L9F96YI1smP83Bicr4yQhhXVjV3JIc1YYsTBgOfaYZ0pkZ8si8BEbNMy3Okjjf2psHjuwQ_TzDFUglOP0MBVz)
    
 After loading the key  click directly to '**save private key**' ***BUT NOT 'generate' +  'save private key'*** , because the latter causes 'key refuse' 
    
4.  Select your .pem file for the key pair that you specified when you launched your instance, and then choose Open. Choose OK to dismiss the confirmation dialog box.
    
5.  Choose Save private key to save the key in the format that PuTTY can use. PuTTYgen displays a warning about saving the key without a passphrase. Choose Yes.
    
6.  Specify the same name for the key that you used for the key pair (for example, my-key-pair). PuTTY automatically adds the .ppk file extension.
    

#### Connect to your server with Putty 

1.  Start PuTTY (from the Start menu, choose All Programs > PuTTY > PuTTY).
    
2.  In the Category pane, select Session and enter ec2-user@your__Public DNS (IPv4) 
THe public_DNS  can be easily found here (image below). [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/putty.html?icmpid=docs_ec2_console](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/putty.html?icmpid=docs_ec2_console) 

![image.png](https://mail.google.com/mail/u/0?ui=2&ik=ac72f488f7&attid=0.1&permmsgid=msg-a:r-7001279932953989352&th=1744fdbd23ef9542&view=fimg&sz=s0-l75-ft&attbid=ANGjdJ_cX3nTZY3lpasz722dRExbPTNxIIe0PfL2qTTDnGfFwc1aJRrmPoEOSKsrRoKKjUVx9AkKfuGRbRBqxcOodTMHTO1LWbqQno4UofAmJ_FKlWrICMEUuUuagxQ&disp=emb&realattid=ii_kell3qoa0)  

3.  Under Connection type, select SSH and double check that the port is 22 
    
4.  In the Category pane, expand Connection, expand SSH, and then select Auth.
    
5.  Click Browse and Select the .ppk file that you generated for your key pair, and then choose Open. ![Putty_Auth](https://lh5.googleusercontent.com/Zp5QpERGbGqNcAmE5cx_i_frKyQ_12GEy2opZFG3j9aUxTZHTaqIJCrkapATC4SzhLpkeG3eIrtD0s7depAwTYcOCJlL5Zx2dlM_I3YfUT4Vfynq-0EiFV6rpSfTOeREkpV9XKm5)
    
6.  If this is the first time you have connected to this instance, PuTTY displays a security alert dialog box that asks whether you trust the host you are connecting to. Choose Yes.
    
7.  You should now be logged into your Instance

## Alternatively, connect via a chrome extension
See info here:
http://www.mattburns.co.uk/blog/2012/11/15/connecting-to-ec2-from-chromes-secure-shell-using-only-a-pem-file/

Note: if your TA has provided you with a temporary instance to use, this information will be different.


After you have connected to your instance through the terminal, move on to Part 2 to learn about the bash shell, grab a copy of this lab from github, and then conduct parts of Lab 1 from the command line.

NOTE: If you are not able to launch your own instance from AWS, see your TA for instructions.

# You have completed Part I of the lab. 
# For parts II through VIII, navigate to the file "part2.md" in this repository.













<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEwOTY0MTQyMywxMzgyNTgxMjMzLC01OT
c3NjU5NDIsLTI1NDY2MTUwOSw2NzEzNjc3NjIsMTQ1Mjg3NjUx
MywtMTU4MjQ1MTM0MSwtOTY3MjczMzQxLC0xNjYyMzc5NzQ0LC
0xODE4NzU2OCw1NTgwNDExMzIsLTE3NDYyNzkzNjEsMzExNTQ3
ODk0LDE3MDE1Nzk4MzQsNTQxMTU1NjY1LC0xMTY1NzM3NDY4LC
0yMDcwNjc2MDg2LDI4MTMyNDE5MiwtMTc4NDY1MDE1NSwxMjY2
NjU2MDk5XX0=
-->