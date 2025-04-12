### 🛠 Lamp Stack Deployment

---

#### ✅ Setup Instructions

1. **Install ansible**
   ```bash
   sudo apt install ansible
   ```
2. **Create the file structure:**
   ```bash
   mkdir -p lamp-ansible/inventories/dev
   mkdir -p lamp-ansible/roles/{apache,mysql,php,firewall}/tasks
   mkdir -p lamp-ansible/roles/apache/files
   touch lamp-ansible/playbook.yml
   touch lamp-ansible/inventories/dev/hosts
   touch lamp-ansible/roles/apache/tasks/main.yml
   touch lamp-ansible/roles/mysql/tasks/main.yml
   touch lamp-ansible/roles/php/tasks/main.yml
   touch lamp-ansible/roles/firewall/tasks/main.yml
   touch lamp-ansible/roles/apache/files/index.php
   touch lamp-ansible/README.md
   ```

3. **Set up the inventory file**

4. **Write roles tasks as uploaded**

5. **Create the main playbook as uploaded**

6. **Run the playbook:**
```bash
   ansible-playbook -i inventories/dev/hosts playbook.yml
   ```
7. **Open the browser and open http://localhost you should see the apache default page**


---

#### ✅ Inventory Structure Explanation

**The inventory file defines the target hosts and groups for Ansible to use.**

ex :

[web]
localhost ansible_connection=local

web : group name used in the playbook

localhost : is the target host

ansible_connection=local : this to make ansible run commands locally
