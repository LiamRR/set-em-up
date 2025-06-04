# set-em-up

This Ansible project automates the setup of new laptops for team members, supporting both Windows (coming soon!) and Linux operating systems.

## How to Use

1. Clone this repository:
   ```
   git clone <repository-url>
   cd set-em-up
   ```

2. Update the inventory file with your target machine:
   - For local setup, use `localhost`
   - For remote setup, specify the `hostname/IP`

3. Run the playbook:
   ```
   # For Windows machines
   ansible-playbook -i inventory.yml playbook.yml --limit windows

   # For Linux machines
   ansible-playbook -i inventory.yml playbook.yml --limit linux -kK
   ```

4. To install only specific components:
   ```
   ansible-playbook -i inventory.yml playbook.yml -t "dev-tools" -kK
   ```
