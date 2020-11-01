Make sure `gather_facts` is enabled.

Make sure to `include_vars` the following `credentials.yml` in the playbook 
```
ansible_become_method: su
ansible_become_user: root
ansible_become_password: rootpassword
```
`include_vars` take precedence over role `vars`.

#### `vars_files` vs `include_vars`
Include variables from a variable file created statically before running the configuration  
`vars_files: vars.yml`
  
Dynamically include variables (based on a certain criteria or using a loop). Has higher priority than `vars_files` 
`include_vars: vars.yml`  

#### `import_tasks` vs `include_tasks`
Statically import tasks (*paste the tasks right here*)  
`import_tasks: tasks/commands.yml`  
  
Dynamically import tasks with variables/tasks that can change during execution (*tasks cen be looped, skipped and use variables form any asource*)  
`include_tasks: tasks/commands.yml`
