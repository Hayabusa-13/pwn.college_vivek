# CITADEL CTF (write-ups)


## Challenge 
1. Test of Sweetness 
### Solve
1. To solve this , i inspected the page and went to the apllication tab and then from there i opened the cookies and in there i changed the value from 'user' to admin and then the flag was given after refreshing the page

## Challenge                                                    
2. The Robot's Trail 
### Solve
1. First I inspected the website and went into the source code and  we get a hint to go to robots.txt
     ``` <div class="hidden">
        <p>Start by checking what this site tells search engine bots in <a href="/robots.txt" style="color: #00bcd4;">robots.txt</a></p>
     </div> ```
2. When we go to robots.txt we get a file path i.e  "/file?path=../../etc/passwd"
3. when go to the file path we then again get anther fie path i.e 
"/var/www/html/config.php:/home/webadmin:/bin/bash"
4. When go to the file path we find another path
   "/var/log/apache2/access.log"         
5. From there we get another file path "/proc/self/environ"
6. From there we get another file path "/home/ctf/.secret "
7. From there u go to "/home/ctf/.secret/flag.txt " and get the flag 


## Challenge 
3. Coco Conjecture   
### Solve
1. First i opened an online linux terminal having an public server 
2. Then i ran the command "nc chall_citadel.cryptonitemit.in 61234"
3. And then it showed it me "TOO SLOW " and asked me to do it 269 time to get the flag 
4. I uploaded it in Gemini and asked what it means and then it explained the problem is related to "Collatz conjecture" and then i gave teh given details to it regarding the format of flag it gave me a python code and when i ran it on VScode it gave me the flag 

### Python code

import socket
import re

def steps(n: int) -> int:
    s = 0
    while n != 1:
        if (n & 1) == 0:
            lb = n & -n
            z = lb.bit_length() - 1
            n >>= z
            s += z
        else:
            n = 3 * n + 1
            s += 1
    return s

with socket.create_connection(("127.0.0.1", 420)) as s:
    f = s.makefile("rwb", buffering=0) # turn socket into file object which makes certain operations faster
    while True:
        line = f.readline()
        if not line:
            break
        message = line.decode().strip()
        print(message) # print server data

        m = re.search(r"Round \d+: (\d+)", message)
        if m:
            n = int(m.group(1))
            ans = str(steps(n)) + "\n"
            f.write(ans.encode())
            
        elif "citadel{" in message:
            break # break if flag found in server ouput



## Challenge 
4. schlagenheim

### Solve
1. We get a .wav file but when viewed in an hex editor  we find that its magic bytes show it being MIDI file 
2. From there changing the M1D1 TO MThd and then saving when we play it in Audacity , we get the flag







