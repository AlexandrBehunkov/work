### Общие требования
1. Именование переменных
1.	Имена переменных составляются из слов английского языка (транслитерация русских слов не допускается).
2.	Имена неконстантных переменных, функций состоят из строчных символов (допускается использовать отдельные слова из прописных символов), слова разделятся символом подчеркивания «_».
3.	Имена констант состоят из только прописных символов, для разделения слов используется символом подчеркивания «_».
4.	Должны отсутствовать закомментированные фрагменты программы (допускается временное присутствие подобных фрагментов при наличии подробного комментария с описанием зачем данный блок закомментирован).
5.	Длина строки равна 80 символам. Если строка программного кода не помещается целиком, она разбивается на несколько строк
6.	Абзацный отступ – 4 пробела.   
7.	В строке располагается только один оператор.
8.	Фигурная скобка в таблицах располагается на одном уровне с кодом. 
Пример: 
```sh
system_info = 
    {
    --Содержимое таблицы. 
    }`
```	
9. Начало блока `then` в системных выражениях располагается в той же строке. Конец блока `end` располагается под началом выражения.
Пример: 
```sh
if true then 
  --Какой-то код. 
end
```
10.	Комментарии должны быть предложениями на русском языке, они должны быть хорошо составлены и иметь правильную пунктуацию (предложение на русском языке, заканчивающееся точкой), по возможности без сокращений.
11.	Отсутствует пробел после -- и комментария.
12.	Каждое определение функции отделяется специальным комментарием (80 символов). Это подобно заголовкам разделов. Вид:
```sh
-- -----------------------------------------------------------------------------
```
13.	Каждое определение функций новой таблицы отделяется специальным комментарием.  Вид:
```sh
-- -----------------------------------------------------------------------------
 -- -----------------------------------------------------------------------------
 ```
14.	Комментирование кода должно быть в виде блоков. Начало метки должно находиться на позиции 77-го символа. 
Пример:
```sh
    `--Отделение сыворотки предварительное.
    --Установка частоты перешивания [1], время работы мешалки при
    --периодическом перемешивании [2], время простоя [3].
    elseif m == self.MODES.WHEY_SEPARATION_PRE then
        self:start_heating()
        m_mngr[ m ]:to_step( 1 )

        if self.default == 1 then
            rt[ RT.MIX_SPEED ] =
                comb_par[COMB_PAR.WHEY_SEPARATION_PRE_MIX_FREQ_DEF ]        --1
            rt[ RT.MIX_TIME_ON ] =
                comb_par[ COMB_PAR.MIX_WORK_TIME_MIXING ]                   --2
            rt[ RT.MIX_TIME_OFF ] =
                comb_par[ COMB_PAR.MIX_WAIT_TIME_MIXING ]                   --3
        end
    end`
```
15.Должно использоваться табличное форматирование кода.
Пример:
```sh
   `self.whey_pump    = W1M1
    self.whey_request = WZ2DO2            --Сыворотка запрос.
    self.whey_OK      = WZ2DI2            --Сыворотка ОК.

    self.curd_pump    = H1M1              --Выдача творога.`
```



