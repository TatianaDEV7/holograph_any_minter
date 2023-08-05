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
