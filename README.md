# Домашнее задание «Организация сети» — Лугинина Виктория

Зона: `ru-central1-a`

- VPC `netology-vpc`
- subnet `public` `192.168.10.0/24`
- NAT-инстанс `192.168.10.254`, image `fd80mrhj8fl2oe87o4e1`
- VM `public-vm` с публичным IP
- subnet `private` `192.168.20.0/24`
- route table `nat-route`: `0.0.0.0/0` → NAT
- VM `private-vm` только с внутренним IP

Манифесты: `main.tf`, `variables.tf`, `versions.tf`

## Ресурсы

![output](screenshots/01-output.png)
![subnets](screenshots/02-subnets.png)
![routes](screenshots/03-routes.png)
![instances](screenshots/04-instances.png)

## Интернет с public-vm

![public ping](screenshots/05-public.png)

## Интернет с private-vm через public-vm

`curl ifconfig.me` показывает публичный IP NAT-инстанса.

![private ping](screenshots/06-private.png)
