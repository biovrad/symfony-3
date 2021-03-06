## 5.6 Закрытые непубличные сервисы

При разработки приложений часто будет создаваться большое количество небольших сервисов, каждый с одной единственной зависимостью. Более сложные высокоуровневые сервисы будут использовать их в качестве внедряемых зависимостей. А нльбольшие низкоуровневые сервисы не предназначены для того, чтобы их использовать самостоятельно. В таких случаях правильно будет закрыть прямой доступ к низкоуровневым сервисам и пометить их как “непубличные”:

```
services:   
    some_service:        
        class: AppBundle\Service\SomeService        
        public: false
```

Если сервис публичный (по-умолчанию), то он будет создан лишь однажды и будет возвращаться один и тот же его экземпляр. Если сервис приватный (параметр "public" установлен в "false"), то он может иметь несколько экземпляров одновременно.