### 3. Для подключения дополнительного репозитория MySQL можно выполнить следующие шаги:

- Откроем терминал и перейдем в режим суперпользователя с помощью команды:

```
sudo su
```

- Добавим ключ репозитория с помощью команды:

```
wget -O- https://repo.mysql.com/RPM-GPG-KEY-mysql-2022 | sudo apt-key add -
```

- Добавим репозиторий MySQL в систему с помощью команды:

```
echo "deb http://repo.mysql.com/apt/ubuntu/ $(lsb_release -sc) mysql-8.0" | sudo tee /etc/apt/sources.list.d/mysql.list
```

- Обновим список пакетов с помощью команды:

```
sudo apt update
```

- Установим любой пакет из репозитория MySQL, например, пакет `mysql-shell`, с помощью команды:

```
sudo apt install mysql-shell
```

### 4. Для установки и удаления deb-пакета с помощью dpkg можно выполнить следующие шаги:

- Скачаем deb-пакет, например, Midnight Commander (MC), с помощью команды:

```
wget http://archive.ubuntu.com/ubuntu/pool/universe/m/mc/mc_4.8.25-2ubuntu2_amd64.deb
```

- Установим deb-пакет с помощью команды:

```
sudo dpkg -i mc_4.8.25-2ubuntu2_amd64.deb
```

- Если в процессе установки возникнут ошибки, которые необходимо исправить, выполним команду:

```
sudo apt --fix-broken install
```

- Удалим установленный пакет с помощью команды:

```
sudo dpkg -r mc
```