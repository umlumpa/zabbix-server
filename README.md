# Zabbix сервер - контроль над сервисами

## на примере пакета zabbix-server
  * подразумевается, что у вас уже есть проект на GCP, есть созданный bucket для хранения tfstate и собственно установленный на вашей машине terraform (я использовал 0.12.2), а так же доменное имя и зона (я размещаю свою в aws_route53_zone)

### Что надо подготовить:
  * файл terraform.tfvars.example переименовать в terraform.tfvars и прописать там имя проекта с GCP (и ключи от aws - если делать как у меня)
  * в файле vars.tf (переименовать с example) указать кол-ко витруальных машин (если нужно как-то по другому) и регион (если нужен другой)

### Что получаем на выходе
  1. установленный и готовый к работе zabbix-server и сколько-то машин с агентами для тестирования
  2. смените на сервере тайм-зону (если вы не земляк с Новосибирска) (в файле scripts/zabconf/apache2.conf - если перед установкой)

### Видео-урок
  * Запись по работе с проектом можно посмотреть [тут](https://youtu.be/)
  * Этот и много других уроков [тут](vk.com/realmanual)

##### Автор
 - **Vassiliy Yegorov** - *Initial work* - [vasyakrg](https://github.com/vasyakrg)
 - [сайт](vk.com/realmanual)