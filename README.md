# Ansible Cloud examples

![Ansible Lint](https://github.com/nleiva/ansible-cloud/workflows/Ansible%20Lint/badge.svg)


Proper documentation in the works.


## Dependencies:

### Python libraries

```bash
pip3 install <>
```

### Collections

```bash
ansible-galaxy collection install -r collections/requirements.yml
```

### Roles

```bash
ansible-galaxy role install -r roles/requirements.yml
```

While both roles and collections can be specified in one requirements file, they need to be installed separately. The `ansible-galaxy role install -r requirements.yml` will only install roles and `ansible-galaxy collection install -r requirements.yml -p ./` will only install collections. See [Installing roles and collections from the same requirements.yml file](https://docs.ansible.com/ansible/latest/galaxy/user_guide.html#installing-roles-and-collections-from-the-same-requirements-yml-file).

### Run in Playbook in an Execution Environment

#### Create Execution Environment image with Ansible builder

Image details in [execution-environment.yml](execution-environment.yml). This is optional, you can pull the image from [quay.io/nleiva/ee_general_image](https://quay.io/repository/nleiva/ee_general_image). 

```bash
ansible-builder build -t quay.io/nleiva/ee_general_image
```

