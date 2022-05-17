# Ansible playbooks
## SSH key generation
* ansible-playbook -i hosts ssh_key_generation.yml --ask-pass

Создает ключ для без парольного подключения

## Technical_characteristics_of_the_host
* ansible-playbook -i hosts technical_characteristics_of_the_host.yml

Собирает данные о количестве ядер, объеме ОЗУ и объеме дискового пространства, формирует json объект. Пример:
``` 
ok: [csgo] => {"ansible_facts": {"result_dict": {"CPU_core": "ansible_facts['processor_cores']", "RAM": "ansible_facts['memory_mb']['real']['total']", "disk_memory_size": "disk_memory_size", "hostname": "docker"}}, "changed": false}
```