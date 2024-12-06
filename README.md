
# GitLab Installation and Configuration Guide

Ansible project to deploy our own Gitlab and Postgres service. Initiative of a course in devops in Efrei school

## Steps

### Step 1: Clone repo
Clone your Ansible GitLab repository:
```bash
git clone https://github.com/marieesss/ansible-gitlab-postgre.git
cd ansible-gitlab-postgre
```

---

### Step 2: Set Up Inventory
Edit the `inventory` file in the project root:
```yaml
all:
  hosts:
    192.168.191.131
```
Replace `192.168.191.131` with the IP of your target host.

---

### Step 3: Deploy Using Ansible
Run the Ansible playbook:
```bash
ansible-playbook -i inventory playbook.yml
```

---

### Step 5: Access GitLab
1. Open your browser and navigate to the external URLspecified in Ansible logs (e.g., `http://192.168.191.131:8080`).
2. Log in with the following default credentials:
   - Username: `root`
   - Password: (Refer to `/etc/gitlab/initial_root_password` inside the container for the generated password or in the ansible logs) 

