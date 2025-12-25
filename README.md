# ansible_vm

## Описание проекта
Ansible роли для базовой раскатки VM. 


## Пример использования

```
git clone https://github.com/rokhman-lsk/ansible_vm.git
```

```
cd ansible_vm
```

```
python3 -m venv .venv
```

```
source .venv/bin/activate
```

```
# Только для раскатки
pip3 install -r requirements.txt

# Для разработки 
pip3 install -r requirements_dev.txt
```

```
# Линтеры
yamllint -c .yamllint.yml -f colored inventories roles
ansible-lint -p --force-color -c .ansible-lint.yml

```

```
ansible-playbook configure_vm.yml -i ./inventories/test/hosts.yml -t users-management -l test.tech  --check --diff --user almalinux --private-key ~/.ssh/private_key --ask-vault-pass
```

