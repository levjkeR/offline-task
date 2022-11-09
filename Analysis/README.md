# Software Analysis
____
### Задание
Проведите анализ ПО, ответив на следующие вопросы:

* Несёт ли угрозу пользователю данное ПО? Если да, то какую?
* Какими инструментами\методиками пользовались при проведении анализа, сколько примерно занял время анализ?
____
### Краткое резюме по PC Cleaner
Время потраченное на анализ *~2 часа*. Долгое время искал нестандартное поведение в IDA  
Основной отчет лежит в файле [Report PC Cleaner](https://github.com/levjkeR/offline-task/blob/main/Analysis/Report%20PC%20Cleaner.pdf)
> Несёт ли угрозу пользователю данное ПО? Если да, то какую?

С помощью статического и динамического анализа подозрительное поведение не выявлено, 
кроме того, что программа сама по себе является твикером-сканером системы и собирает телеметрию. 
Следовательно, ПО является легитимным, но нежелательным к установке, потому что непосредственно 
влияет на работу других программ и/или системы.

>Какими инструментами\методиками пользовались при проведении анализа, сколько примерно занял время анализ?

- IDA Pro
- PEstudio
- Process Monitor
- ProcessHacker2
- Autoruns
- RegShot
- Wireshark

### Краткое резюме по PC OptimizerPro
Время потраченное на анализ *~30 минут*   
Основной отчет лежит в файле [Report PC OptimizerPro](https://github.com/levjkeR/offline-task/blob/main/Analysis/Report%20PC%20OptimizerPro.pdf)
> Несёт ли угрозу пользователю данное ПО? Если да, то какую?

ПО является сканером-оптимайзером системы, относится в категории нежелательных к использованию. 
PCOptimizerPro вынуждает пользователей оплатить 
лицензию, чтобы пользоваться функционалом очистки системы.

>Какими инструментами\методиками пользовались при проведении анализа, сколько примерно занял время анализ?

- IDA Pro
- PEstudio
- Process Monitor
- Autoruns
- RegShot
- Wireshark
- x64dbg

----
### Оффтоп
Изначально при решении задачи пользвался методами статического анализа для поиска
функций для работы с сокетами, но позднее сменил решение в пользу динамического 
анализа. Не стал использовать INetSim