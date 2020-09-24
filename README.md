# Ansible-UserCreation
A simple script to create users on Linux Machine with a password.

How to create the password, according to Ansible website https://docs.ansible.com/ansible/latest/reference_appendices/faq.html#how-do-i-generate-encrypted-passwords-for-the-user-module. In my opinion the best/easy way is to perform using python.

```
pip install passlib
python -c "from passlib.hash import sha512_crypt; import getpass; print(sha512_crypt.using(rounds=5000).hash(getpass.getpass()))"
```
