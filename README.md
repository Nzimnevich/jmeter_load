# jmeter_load


Линейная:

Настройки:
<img width="1208" height="529" alt="Снимок экрана 2025-10-28 в 13 50 24" src="https://github.com/user-attachments/assets/169b153e-3edd-4568-91b2-3c1365a86f8f" />


Графики:

<img width="881" height="711" alt="Снимок экрана 2025-10-28 в 13 50 34" src="https://github.com/user-attachments/assets/bbd48cc0-5a26-4e63-ae0e-ddf3374bd8c5" />
<img width="1254" height="431" alt="Снимок экрана 2025-10-28 в 13 50 52" src="https://github.com/user-attachments/assets/484f4f29-a2db-473d-a831-88ec007a5184" />



Вывод:

Ступенчатая:

Настройки:

<img width="1206" height="722" alt="Снимок экрана 2025-10-28 в 15 19 39" src="https://github.com/user-attachments/assets/96693ce0-9fb3-431f-97dd-468fbf964923" />


Графики:

<img width="884" height="720" alt="Снимок экрана 2025-10-28 в 17 17 50" src="https://github.com/user-attachments/assets/4d2914fb-0e19-4f66-9d93-e30bd1688347" />

<img width="889" height="367" alt="Снимок экрана 2025-10-28 в 17 17 57" src="https://github.com/user-attachments/assets/40ddff9d-984f-4655-b281-555ae7ba8d26" />


Вывод:


## Ключевые метрики:

**Для комментов:**
- Samples: 16498 запросов
- Average: 70 ms (среднее время)
- Median: 79 ms (медиана)
- 90% Line: 86 ms (90% запросов быстрее)
- Max: 400 ms (максимум)
- Error: 0%
- Throughput: 100.96 req/sec

**Для постов:**
- Samples: 16781 запросов  
- Average: 603 ms ❗ (довольно много)
- Max: 49607 ms ❗❗ (49 секунд!)
- Error: 287 ошибок
- Throughput: 139.33 req/sec

## Анализ:

1. **Комменты, альбомы, todos** - работают нормально (70-80 ms)
2. **Посты** - проблемный эндпоинт:
   - Среднее время 603 ms (в 8 раз медленнее)
   - Максимум 49 секунд! 
   - Есть ошибки (287 штук)

## Выводы:

- Система **не выдерживает** нагрузку на эндпоинт **Посты**
- Остальные эндпоинты стабильны
- Пропускная способность хорошая (~100-140 req/sec)


Нужно смотреть почему **Посты** так тормозят - возможно, база данных не справляется или есть блокировки.

