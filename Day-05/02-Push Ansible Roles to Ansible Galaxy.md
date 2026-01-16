



# Push your Ansible roles to Ansible Galaxy
============================================

1. Make sure your role is structured correctly. The basic structure should look like this:

```
my_role/
├── defaults/
│   └── main.yml
├── files/
├── handlers/
│   └── main.yml
├── meta/
│   └── main.yml
├── tasks/
│   └── main.yml
├── templates/
├── tests/
│   ├── inventory
│   └── test.yml
└── vars/
    └── main.yml
```




2. Make sure ansible-galaxy CLI exists

```
ansible-galaxy --version
```




3. Push Your Role to GitHub

```
cd <role-name>
git init
git remote add origin <https://github.com/your_github_username/my_role.git>
git remote -v
git add .
git commit -m "Initial commit"
git push -u origin main
```





4. Go to Ansible Galaxy Collections Section and There is an Option API Token Click on That ->  Load Token  & There will be an Option to Copy the API Token





5. Import the Role to Ansible Galaxy

```
ansible-galaxy role import <your_github_username> <role-name> --token  <token which we have copied above>
```





6. Now When we go to the Roles -> Role Namespaces  -> We Can See the Role Which we Have Published.











