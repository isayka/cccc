# Bounded Contexts
## Customer
Данные клиентов, договоры
## Wallet
кошельки счета балансы блокировки
## Payment
создание платежа, резервирование, списание
## CoreBanking
легаси банкинг
## Notification
нотификации (sms push email)
## AntiFraud
 антифрод, скоринг риска.
## Merchant
Интеграция с внешними системами, сервисы магазины
# Context Map
```mermaid
flowchart LR
	Payment-->|Customer/Supplier|Customer
	Payment-->|Customer/Supplier|Wallet
	Payment-->|Open Host Service|Merchant
	Payment-->|ACL|CoreBanking
	Payment-->|Customer/Supplier|AntiFraud
	Payment-->|Published Language|Notification
	AntiFraud-->|Customer/Supplier|Wallet
	AntiFraud-->|Customer/Supplier|Customer
	Notification-->|Customer/Supplier|Customer
```
