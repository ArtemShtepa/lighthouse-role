Lighthouse-role
===============

������������� ��� ���������������� ������������ ������ ��� ����������� **SystemD** ��� ������������� VK Lighthouse

����������
----------

- **lighthouse_path** - ���� �������� ������ ������� Lighthouse

- **clickhouse_host**: - ���� Clickhouse ��� ��������� �������.

- **clickhosue_port**: - ���� Clickhouse ��� ��������� �������.

- **clickhosue_user**: - ������������ Clickhouse ��� ��������� �������.

- **clickhosue_password**: - ������ ������������� ������������ Clickhouse.

������ �������������
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
