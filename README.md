# Vector Role

Роль для установки и запуска Vector.

### Что делает роль:
- Создает пользователя и группу `vector`
- Создает нужные каталоги для конфигов и данных
- Скачивает бинарник нужной версии и кладет в `/usr/bin`
- Копирует конфиг и настраивает systemd-сервис
- Запускает сервис `vector`

### Переменные по умолчанию (`defaults/main.yml`):
- `vector_version: "0.34.0"` — версия Vector
- `vector_config_dir: "/etc/vector"` — путь к конфигурации
- `vector_data_dir: "/var/lib/vector"` — директория для данных
- `vector_log_dir: "/var/log/vector"` — директория для логов

### Пример вызова:
```yaml
- hosts: all
  roles:
    - vector-role
