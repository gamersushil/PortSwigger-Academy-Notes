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




