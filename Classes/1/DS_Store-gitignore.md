Дарья Максимова подготовила этот документ  [https://github.com/creaciond/digital_literary_studies/blob/master/DS_Store-gitignore.md](https://github.com/creaciond/digital_literary_studies/blob/master/DS_Store-gitignore.md) : 

# Про .DS_Store
Специально для счастливых обладателей машин на Mac OS X :)

## Что это такое?
Возможно, когда вы коммитили ваши файлы и папки через командную строку, вместе с тем, что вы _ожидали_ увидеть (папки и файлы), в репозитории вы увидели странный файл, который называется ```.DS_Store```. Не исключено, что вы уже начали нервничать по этому поводу.

```.DS_Store``` — это **системный** файл, в котором лежат пользовательские настройки текущей папки в духе "какие иконки использовать" и "как сортировать файлы в папке" (а сам DS_Store расшифровывается как _Desktop Service Store_). Его создаёт система, чтобы папка каждый раз выглядела именно так, как вы хотите.

Обычно вы не видите этот файл. Это происходит, потому что Mac OS X скрывает от пользователя все файлы и директории, которые начинаются с точки (а это как раз про DS_Store). Такие файлы называются **скрытыми**.

Когда мы создаём коммит, мы используем строку типа ```git add *``` или ```git add .```, то есть добавляем в коммит _все_ файлы (и подпапки текущей папки, если используем вариант со звёздочкой), включая скрытые. Поэтому в репозитории и отображается ```.DS_Store```.

## Как убрать .DS_Store из репозитория?
Для этого воспользуемся удобной штукой, которая называется _gitignore_. Она позволяет указать файлы и папки, которые не нужно коммитить (что, на самом деле, вытекает из её названия: _git_ + _ignore_ :)

### Своими руками
Откройте любой текстовый редактор и пропишите в нём **пути** к файлам и папкам, которые вы не хотите коммитить. Один файл/папка = одна строка. Это должно выглядеть примерно так:

![Прописываем путь](https://pp.userapi.com/c831109/v831109092/54c38/MTK3Yidf8yA.jpg "Прописываем путь")
_Я использую Sublime Text_

После этого сохраните этот файл в папке, из которой коммитите в репозиторий. Дайте ему имя ```.gitignore``` (да-да, именно так, начиная с точки!).

![Называем файл](https://pp.userapi.com/c831109/v831109092/54c41/j5RJhd09p3M.jpg "Называем файл")

Система предупредит вас о том, что вы собираетесь создать скрытый файл, который не будет видно. Мы теперь прошаренные и знаем, что так бывает, поэтому уверенно (принимаем условия данного лицензионного соглашения) нажимаем, что хотим начать с точки.

![Предупреждение](https://pp.userapi.com/c831109/v831109092/54c48/8dVqoil85cI.jpg "Предупреждение")

Создайте коммит (```git add```, ```git commit```, всё как всегда) и запушьте (```git push```) его в ваш репозиторий. Не забудьте дать коммиту осмысленное сообщение.

Готово, вы восхитительны!

### Автоматически (при создании репозитория)
При создании репозитория вы можете использовать ```.gitignore```, который заранее собран усилиями тех, кто уже кодил на том или ином языке программирования. Это поможет не коммитить лишний "мусор", который возникает при запуске программ.

При создании репозитория найдите в списке нужный вам язык и кликните по нему (можно использовать поиск).

![Авто-гитигнор](https://pp.userapi.com/c831109/v831109092/54c50/oe2IIKp6mmw.jpg "Авто-гитигнор")

_Внимание на левый нижний угол_

Готово, вы восхитительны!

> Важно: уже созданный gitignore можно и нужно редактировать, если вам это нужно.

## Как настроить систему так, чтобы скрытые файлы отображались?

Следуйте [инструкции](https://ochprosto.com/kak-pokazat-skrytye-fajly-na-mac-os/). Если она вам не нравится, загуглите "отображение скрытых файлов mac os x" :)