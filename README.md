

This playbook will install Docker and containers WordPress with MySQL into your remote Ubuntu host.



Prerequisites:
  - Controller node with Ansible installed.

Execution steps:

  1. Replace the *test1* IP address in the **hosts** file with the target IP of your remote ubuntu host.
  ```
      [test_servers]
      test1 ansible_host=3.125.53.203
  ```
  2. Encrypt *mysql root password* and *mysql wordpress password* with Ansible vault and place the results to the **/host_vars/test1** accordingly:
  ```
      ansible-vault encrypt_string 'your_mysql_password' --name 'mysql_root_password'
      ansible-vault encrypt_string 'your_wordpress_password' --name 'mysql_wordpress_password'
  ```
  3. Run the playbook wp.yml
  ```
      ansible-playbook --ask-vault-pass wp.yml
  ```
As the default WP will run on 8001 port.
