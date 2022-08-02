Lighthouse-role
===============

Предназначена для конфигурирования операционных систем под управлением **SystemD** для использования VK Lighthouse

Переменные
----------

- **lighthouse_path** - Путь хранения файлов статики Lighthouse

- **clickhouse_host**: - Хост Clickhouse для просмотра метрики.

- **clickhosue_port**: - Порт Clickhouse для просмотра метрики.

- **clickhosue_user**: - Пользователь Clickhouse для просмотра метрики.

- **clickhosue_password**: - Пароль авторизуемого пользователя Clickhouse.

Пример использования
--------------------

```yaml
- name: Install and configure Lighthouse
  hosts: lighthouse
  become: true
  vars:
    lighthouse_path: "/home/user/lighthouse"
    clickhouse_host: groups['clickhouse'][0]
  roles:
    - lighthouse_role
```
