Make sure `gather_facts` is enabled.

Make sure to `include_vars` the following `credentials.yml` in the playbook 
```
ansible_become_method: enable
ansible_become_user: myuser
ansible_become_password: mypassword
```
`include_vars` take precedence over role `vars`.


Statically import tasks (*paste the tasks right here*)
`import_tasks: tasks/commands.yml`  

Dynamically import tasks with variables/tasks that can change during execution (*tasks cen be looped, skipped and use variables form any asource*)
`include_tasks: tasks/commands.yml`
