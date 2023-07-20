#### APPRENTICE
###### Lab: File Path Traversal, Simple Case

*This lab contains a file path traversal vulnerability in the display of product images. To complete the lab, I needed to retrieve the contents of the "/etc/passwd" file.*

**Solution:**
1. Click on any image and observe the parameter. When a user clicks on any image, the parameter looks like "filename=31.jpg".
2. Now, attempt to access the "/etc/passwd" file by modifying the parameter to "../../etc/passwd".
3. `<URL>?filename=../../etc/passwd`
        Congratulations, you solved the lab!

#### PRACTITIONER
###### Lab: File path traversal, traversal sequences blocked with absolute path bypass

*This lab contains a file path traversal vulnerability in the display of product images. The application blocks traversal sequences but treats the supplied filename as being relative to a default working directory. To solve the lab, retrieve the contents of the `/etc/passwd` file.*

**Solution:**
1. Click on any image and observe the parameter. When a user clicks on any image, the parameter looks like "filename=22.jpg".
2. Now, attempt to access the "/etc/passwd" file by modifying the parameter to "/etc/passwd".
3. `<URL>?filename=/etc/passwd`
        Congratulations, you solved the lab!

#### PRACTITIONER
###### Lab: File path traversal, traversal sequences stripped non-recursively

*This lab contains a file path traversal vulnerability in the display of product images. The application strips path traversal sequences from the user-supplied filename before using it. To solve the lab, retrieve the contents of the `/etc/passwd` file.*

**Solution:**
1. Click on any image and observe the parameter. When a user clicks on any image, the parameter looks like "filename=22.jpg".
2. Now, attempt to access the "/etc/passwd" file by modifying the parameter to "....//....//....//etc/passwd".
3. `<URL>?filename=....//....//....//etc/passwd`
        Congratulations, you solved the lab!

#### PRACTITIONER
###### Lab: File path traversal, traversal sequences stripped with superfluous URL-decode

*This lab contains a file path traversal vulnerability in the display of product images.The application blocks input containing path traversal sequences. It then performs a URL-decode of the input before using it.To solve the lab, retrieve the contents of the `/etc/passwd` file.*

**Solution:**
1. Click on any image and observe the parameter. When a user clicks on any image, the parameter looks like "filename=22.jpg".
2. Now, attempt to access the "/etc/passwd" file by modifying the parameter to "..%252f..%252f..%252fetc%252fpasswd".
3. `?filename=..%252f..%252f..%252fetc%252fpasswd`
        Congratulations, you solved the lab!

#### PRACTITIONER
###### Lab: File path traversal, validation of start of path

*This lab contains a file path traversal vulnerability in the display of product images.The application transmits the full file path via a request parameter, and validates that the supplied path starts with the expected folder. To solve the lab, retrieve the contents of the `/etc/passwd` file.*

**Solution:**
1. Click on any image and observe the parameter. When a user clicks on any image, the parameter looks like "filename=22.jpg".
2. Now, attempt to access the "/etc/passwd" file by modifying the parameter to "/var/www/images/../../../etc/passwd".
3. `?filename=/var/www/images/../../../etc/passwd`
        Congratulations, you solved the lab!

#### PRACTITIONER
###### Lab: File path traversal, validation of file extension with null byte bypass

*This lab contains a file path traversal vulnerability in the display of product images. The application validates that the supplied filename ends with the expected file extension. To solve the lab, retrieve the contents of the `/etc/passwd` file.*

**Solution:**
1. Click on any image and observe the parameter. When a user clicks on any image, the parameter looks like "filename=22.jpg".
2. Now, attempt to access the "/etc/passwd" file by modifying the parameter to "../../../etc/passwd%00.jpg".
3. `?filename=../../../etc/passwd%00.jpg`
        Congratulations, you solved the lab!



