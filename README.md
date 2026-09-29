# Домашнее задание «Организация сети» — Лугинина Виктория

Зона: `ru-central1-a`

- VPC `netology-vpc`
- subnet `public` `192.168.10.0/24`
- NAT-инстанс `192.168.10.254`, image `fd80mrhj8fl2oe87o4e1`
- VM `public-vm` с публичным IP
- subnet `private` `192.168.20.0/24`
- route table `nat-route`: `0.0.0.0/0` → NAT
- VM `private-vm` только с внутренним IP

Манифесты: [`main.tf`](main.tf), [`variables.tf`](variables.tf), [`versions.tf`](versions.tf)

## Ресурсы

![1.png](https://github.com/victorialugi/net/blob/main/1.png)
![2.png](https://github.com/victorialugi/net/blob/main/2.png)


## Интернет с public-vm

![3.png](https://github.com/victorialugi/net/blob/main/3.png)


## Интернет с private-vm через public-vm

`curl ifconfig.me` показывает публичный IP NAT-инстанса.

![4.png](https://github.com/victorialugi/net/blob/main/4.png)

