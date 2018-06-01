# Почта

Для отправки почты по SSL можно установить stunnel

конфигурационный файл /usr/local/etc/stunnel/stunnel.conf

```text
client = yes
[ssmtp]
accept = 465
connect = smtp.gmail.com:465
```

файл службы /etc/init.d/[stunnel](https://yadi.sk/i/lvB2f17G3WnsAj)

Так же для отправки почты необходимо настроить права ACL.

