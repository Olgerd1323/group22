# Homework ADB 
1. Отобразить подключённый девайс в консоли			`adb devices`
2. Вывести адрес приложения todolist в системе Android			`adb shell pm list packages | select-string "todolist"`
3. Установить .apk файл приложениия todolist на телефон с компьютера через  ADB			`adb install /path/todolist.apk`
4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде    `adb shell screencap /path_on_device/todolist.png`
5. Вывести в консоль логи приложения todolist			`adb logcat | select-string "todolist"`
6. Скопировать логи приложения todolist на компьютер `adb logcat | select-string "com.android.todolist" > /path_to_save/todolist.log`
7. Удалить приложение todolist с телефона через ADB			`adb uninstall com.android.todolist`
