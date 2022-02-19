
Prerequisites:
  - Controller node with Ansible installed.

1. Replace the *test1* IP address in the **hosts** file with the target IP of your remote ubuntu host.
```
[test_servers]
test1 ansible_host=3.125.53.203
```
3. Encrypt *mysql root password* and *mysql wordpress password* with Ansible vault:
```

```
4. Run the wp.yml
```
```
