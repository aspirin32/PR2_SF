FAQ:
1. Где располагается репозиторий с кодом, как посмотреть существующий код;
    https://github.com/aspirin32/PR2_SF.git
2. Как устроен процесс внесения своих изменений в основную кодовую базу;
    Код добавляется в ветку main только через PR c обязательным согласованием и CodeReview
3. Каковы правила именования веток;
    F_* – ветки для доработок
    BF_* – ветки для BugFixes
    D_* – ветка разработки
    Release_* – ветки релизов и только из них осуществляем PR в Main
4. Как настроить свою среду разработки, требуется прикрепить ссылку на лежащий в проекте конфиг;
    Пример настройки: 
        https://github.com/aspirin32/PR2_SF/blob/da664f1a31ebfa777838ec6b172300a385a37a83/config
        Local находится в каталоге .git репозитория: .git/config
        Global находится ~ /.gitconfig
5. Инструкция для младших сотрудников по слиянию веток, какие команды надо выполнить, чтобы:
    - создать свою ветку из main;
        Git branch <наименование ветки в соответсвии с правилами п.3>
    - перейти на новую ветку;
        Git checkout <новая ветка>
    - внести изменения в нее;
        Работаем с файлами, далее командой git add добавляем изменения,
        Далее git commit – подробно описываем изменения и дорабоктки,
        Git push origin <новая созданная ветка> - сливаем в удаленный репозиторий в свою ветку.
        Далее делаем merge в ветку develop и далее по аналогии в ветку своего релиза, merge релиза проверяют коллеги
    - слить эти изменения с основной кодовой базой.
        В main создаем Pull Request в удаленном репозитории, PR обязательно согласовывается и только после возможен merge в main.
