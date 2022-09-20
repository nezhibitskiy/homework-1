# Домашнее задание по обеспечению качества
## Команда KuragaTeam

## Содержание

1. [Проект](#ссылка-на-проект)
2. [Тестовое окружение](#тестовое-окружение)
3. [Тестирование](#тестирование)


## Ссылка на проект
[Movie-Space](https://movie-space.ru/)
### Описание проекта
Movie Space -  это стриминговый сервис, предназначенный для просмотра любимых фильмов и сериалов на любых устройствах
## Тестовое окружение
OC: `Ubuntu 20.04.5 LTS`. 

Имя процессора:	`Intel® Core™ i5-7300HQ CPU @ 2.50GHz × 4`

Тип монитора: `TN+film, 15.6`  

Разрешение:	`1920 x 1080`. 

Браузер + версия: `Google Chrome Версия 104.0.5112.101 (Официальная сборка), (64 бит)`. 

# Тестирование
Видеоплеер. Показ сериалов (основной функционал сервиса)

![image](https://user-images.githubusercontent.com/71338063/191306327-f552e6cb-0d34-4982-ae26-9eea54484e64.png)

### Тесты
1. Остановка воспроизведения по нажатию на кнопку "Pause" и смена кнопки "Pause" на кнопку "Play"
![image](https://user-images.githubusercontent.com/71338063/191307480-146873c1-e4c1-415e-9237-659d869b000b.png)
2. Запуск остановленного воспроизведения по нажатию на кнопку "Play" и смена кнопки "Play" на кнопку "Pause"
![image](https://user-images.githubusercontent.com/71338063/191307605-2284ac66-f953-4223-ac41-60055dfcbed9.png)
3. Перемотка воспроизведения на 10 секунд назад при нажатии кнопки "Перемотать воспроизведение на 10 секунд назад"
4. Перемотка воспроизведения на 10 секунд вперед при нажатии кнопки "Перемотать воспроизведение на 10 секунд вперед"
5. Отключение звука при нажатии на кнопку "Отключение звука" и смена кнопки "Отключение звука" на кнопку "Включение звука". Смена значения ползунка громкости на 0 значение.

![image](https://user-images.githubusercontent.com/71338063/191310132-272935ec-51a1-4423-8fd4-fa74e39fd7e4.png)

6. Включение звука при нажатии на кнопку "Включение звука" и смена кнопки "Включение звука" на кнопку "Отключение звука". Смена значения ползунка громкости на значение, соответствовавшее до отключения звука.

![image](https://user-images.githubusercontent.com/71338063/191310107-5c791dcd-da7f-4c52-b281-6df79b771785.png)

7. Соответствующая смена громкости при нажатии на ползунок изменения громкости. Перемещение указателя текущей громкости на выбранное место.
8. **Баг:** Перетягивание текущего указателя громкости в новое положение. 
    
    *Текущее поведение:* указатель перемещается только после отпускания левой кнопки мыши. 
    
    *Ожидаемое поведение:* указатель грмокости следует за указателем мыши
9. Переход в полноэкранный режим по нажитию кнопки "Полноэкранный режим"
10. Переключение на следующую серию при нажатии на кнопку “Следующая серия”
11. Переключение на предыдущую серию при нажатии на кнопку “Предыдущая серия”
12. Перемотка воспроизведения на 10 секунд назад при нажатии клавиши на клавиатуре “Стрелка влево”
13. Перемотка воспроизведения на 10 секунд вперед при нажатии клавиши на клавиатуре “Стрелка вправо”
14. Выход из видеоплеера при нажатии клавиши “Escape” на клавиатуре
15. Баг: Увеличение громкости с помощью клавиш на клавиатуре.

    *Текущее поведение:* не увеличивается громкость при нажатии клавиши “Стрелка вверх” на клавиатуре, не уменьшается громкость при нажатии клавиши “Стрелка вниз” на клавиатуре.
    
    *Ожидаемое поведение:* увеличивается громкость при нажатии клавиши “Стрелка вверх” на клавиатуре, уменьшается громкость при нажатии клавиши “Стрелка вниз” на клавиатуре.
16. Ползунок длительности серии (Кроссфейдер) при наведении на ползунок курсор меняется на поинтер
17. При нажатии на дорожку длительности серии положение бегунка переносится резко на место нажатия справа от ползунка отображается оставшееся время серии
18. *Плохой кейс:* при захвате бегунка, чтобы передвинуть его в определенное место необходимо двигать его вдоль дорожки бегунок при захвате перемещается с задержкой
19. **Баг:** захват бегунка и передвижение его вдоль дорожки

    *Текущее поведение:* не отображается в какую сторону он передвигается
    
    *Ожидаемое поведение:* при захвате бегунка и передвижении его вдоль дорожки отображается в какую сторону он передвигается
    
    серии сезона
при наведении на кнопку серии сезона увеличивается кнопка, курсор меняется на поинтер, отображается окно со списком серий сезона