### About
Minimalist Ansbile script to stand up a Ubuntu Rails server using Nginx

#### Run command
* ansible-playbook -i hosts site.yml

### Setup

ansible.cfg:
Create in root. Make sure to have this with the hosts file name in there

./hosts:
Put the server IP address in there

### site.yml
You can comment out tasks from here

Essentials are
  roles:
    - common
    - deploy-user
    - ruby
    - nginx
    - postgres

### Common Tasks
If you add anything new under roles/common/tasks then you have to import it into main.yml under same folder

### Aliases
See and add any aliases under:
- roles/deploy-user/templates/aliases

### Debug example
- debug:
    msg: User {{ db_user }} DBName {{db_name}} Pwd {{db_password}}


Many thanks to Aleks
