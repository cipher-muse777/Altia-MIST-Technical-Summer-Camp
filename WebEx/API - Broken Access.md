## API - Broken Access
Your friend has set up a platform where you can register and post a private note. Everything is based on an API. Before setting up the Front-End, he asked you to check that everything was secure.

### SOLUTION 
- i first created a new user with new password and then logged in with the new credentials
- then i inspected the site's cookies and noticed that they provided a flask session cookie instead of a jwt token which made me realise that the authentication was session-based
- then i explored the available API endpoint `GET /api/user` which accepted a `user_id` parameter.
- when i typed in user_id as 1 so i got this request url ```link http://api-broken-access.challenge01.root-me.org/api/user``` which when i opened gave me user info about the user i created 
-  so i changed to ```http://api-broken-access.challenge01.root-me.org/api/user/1``` which should theoretically be the admin user, then i got the password in the notes
  <img width="1917" height="1110" alt="image" src="https://github.com/user-attachments/assets/f0987a3c-771b-4671-9ecb-4eb92beeb5b3" />

### FLAG 
RM{E4sy_1d0r_0n_API}

### RESOURCES 
https://owasp.org/API-Security/editions/2023/en/0xa1-broken-object-level-authorization/
