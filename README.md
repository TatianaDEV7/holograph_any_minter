# holograph_any_minter
- Оригинал скрипта https://github.com/1liochka1/build_minter

Данный вариант для тех кто хочет сминтить новую НФТ.
Для FLWR менять не надо.
Что надо менять:
1) В файле **utils.py**
- строка 40. Замение адрес контракта НФТ (пример от нфт под названием [FLWR](https://arbiscan.io/address/0xd4feff615c0e90f06340be95d30e1f397779a184))
```
self.drop_address = Web3.to_checksum_address('0xd4feff615c0e90f06340be95d30e1f397779a184')
```
- строка 123. Замените точно так же адрес:
```
self.nft_address = Web3.to_checksum_address('0xd4feff615c0e90f06340be95d30e1f397779a184')
```


# Установка и настройка
### Установка на Ubuntu
Обновляемся
```
sudo apt update && sudo apt upgrade -y
```
Скачиваем
```
git clone https://github.com/TatianaDEV7/build_minter
```
Заходим в папку со скриптом
```
dir
cd build_minter
```
Устанавливаем pip:
```
apt install python3-pip
pip install tqdm ccxt loguru termcolor telebot pyuseragents tabulate web3==6.4.0 pandas
```
Устанавливаем библиотеки. Для заметки - для этого скриптаустанавливается `web3==6.4.0`
```
pip install -r requirements.txt
```
> На Ubuntu будет ругаться на библиотеку `pywin32==306`. Это нормально, она нужна только для Винды.
## Запуск (только после Настройки)

```bash
# Заходим в папку скрипта
cd /root/build_minter

# Запуск с выводом stdout в командную строку
python3 main.py
# Запуск в фоновом режиме. Записывает логи в файл log.log
nohup python3 main.py > log.log 2>&1 &

# Завершить процесс:
pgrep -a python
kill (номер процесса)
```
