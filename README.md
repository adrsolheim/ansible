Make sure to import the following `vars_file` in the playbook calling the roles
```
ansible_become_method: enable
ansible_become_user: myuser
ansible_become_password: mypassword
``


Statically import tasks (*paste the tasks right here*)
`import_tasks: tasks/commands.yml`  

Dynamically import tasks with variables/tasks that can change during execution (*tasks cen be looped, skipped and use variables form any asource*)
`include_tasks: tasks/commands.yml`
