# TON Reverse engineering for Enterprise Architect
reverse engineering - проектирование Архитектуры проекта путем Реверс инжениринга
https://drive.google.com/drive/folders/1gJf1GLVUnmB5l-t-pViawvKM1FOElPQn

Оригинальный репозитарий TON (Telegram Open Network)  
https://github.com/ton-blockchain/ton

исходные тексты блочейн-платформы TON (Telegram Open Network), с 2017 года развиваемой компанией Telegram Systems LLP  

TON предоставляет набор технологий, обеспечивающих функционирование распределённой сети для работы различных сервисов на базе блокчейна и умных контрактов. 
В ходе ICO проект привлёк более 1.7 млрд долларов инвестиций. 
Исходные тексты включают 1610 файлов, содержащих около 398 тысяч строк кода. 
Проект написан на языке C++ и распространяется под лицензией GPLv2 (библиотеки под LGPLv2).

Помимо блокчейна TON включает также систему P2P-коммуникаций, распределённое хранилище блокчейна и компоненты для хостинга сервисов. TON может рассматриваться как распределённый суперсервер, предназначенный для размещения и предоставления различных сервисов на базе умных контрактов. На базе платформы TON будет запущена криптовалюта Gram, которая кардинально быстрее Bitcoin и Ethereum по скорости подтверждения транзакций (миллионы транзакций в секунду вместо десятков), и способна обрабатывать платежи со скоростью процессинга VISA и Mastercard.

Открытые исходные тексты позволяют принять участие в тестировании проекта и развернуть собственный узел сети, который отвечает за определённую ветку блокчейна. Узел также может функционировать в роли валидатора для подтверждения транзакций в блокчейне. Для определения кратчайшего пути между узлами используется маршрутизация на основе гиперкуба (Hypercube Routing). Майнинг не поддерживается - все единицы криптовалюты Gram сгенерированы разом и будут распределены между инвесторами и стабилизационным фондом.

# Основные компоненты TON:

# TON Blockchain  
TON Blockchain - блокчейн-платформа, способная выполнять тьюринг-полные умные контракты, создаваемые на разработанном для TON языке Fift и выполняемые в блокчейне при помощи специальной виртуальной машины TVM. Поддерживается обновление формальных спецификаций блокчкейна, мультикриптовалютные операции, микроплатежи, офлайновые платёжные сети;  

# TON P2P Network  
TON P2P Network - формируемая из клиентов P2P-сеть, используемая для доступа к TON Blockchain, отправки кандидатов транзакций и приёма обновлений для частей блокчейна, необходимых клиенту. P2P-сеть также может применяться в работе произвольных распределённых сервисов, в том числе не связанных с блокчейном;  

# TON Storage   
TON Storage - Распределённое хранилище файлов, доступное через сеть TON и используемое в TON Blockchain для хранения архива с копиями блоков и снапшотами данных. Хранилище также применимо для размещения произвольных файлов пользователей и сервисов, работающих на базе платформы TON. Отдача данных напоминает торренты;  

# TON Proxy  
TON Proxy - проки-анонимайзер, напоминает I2P (Invisible Internet Project) и используется для скрытия местоположения и адресов узлов сети;  

# TON DHT  
TON DHT - распределённая хэш-таблица, напоминающая Kademlia, и используемая в качестве аналога торрент-трекера для распределённого хранилища, а также как определитель точек входа для прокси-анонимайзера и как механизм поиска сервисов;  

# TON Services  
TON Services- платформа для создания произвольных сервисов (некое подобие сайтов и web-приложений), доступных через TON Network и TON Proxy. Интерфейс сервисов формализован и допускает взаимодействие в стиле браузеров или мобильных приложений. Описания интерфейса и точки входа публикуются в TON Blockchain, а предоставляющие сервисы узлы определяются через TON DHT. Сервисы могут создавать умные контракты в TON Blockchain для гарантирования выполнения определённы обязательств перед клиентами. Полученные от пользователей данные могут сохраняться в TON Storage;  

# TON DNS  
TON DNS - система для назначения имён для объектов в хранилище, умных контрактов, сервисов и узлов сети. Вместо IP-адреса имя преобразуется в хэши для TON DHT;  

# TON Payments  
TON Payments- платформа микроплатежей, которая может применяться для быстрой передачи средств и оплаты за сервисы с отложенным отображением в блокчейне;  

Компоненты для интеграции со сторонними мессенджерами и приложениями для социальных сетей, позволяющие сделать технологии блокчейна и распределённые сервисы доступными для обычных пользователей. Одним из первых массовых приложений, в котором появится поддержка TON, обещают сделать мессенджер Telegram.
