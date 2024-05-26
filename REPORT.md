## Laboratory work IX

Данная лабораторная работа посвещена изучению процесса создания артефактов на примере **Github Release**

```sh
$ open https://help.github.com/articles/creating-releases/
```

## Tasks

- [ ] 1. Создать публичный репозиторий с названием **lab09** на сервисе **GitHub**
- [ ] 2. Ознакомиться со ссылками учебного материала
- [ ] 3. Получить токен для доступа к репозиториям сервиса **GitHub**
- [ ] 4. Выполнить инструкцию учебного материала
- [ ] 5. Составить отчет и отправить ссылку личным сообщением в **Slack**



## Report

```sh
vadim@vadim-VirtualBox:~$ export GITHUB_TOKEN=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
vadim@vadim-VirtualBox:~$ export GITHUB_USERNAME=polenk0
vadim@vadim-VirtualBox:~$ export PACKAGE_MANAGER=apt
vadim@vadim-VirtualBox:~$ export GPG_PACKAGE_NAME=gpg
vadim@vadim-VirtualBox:~$ sudo $PACKAGE_MANAGER install xclip
[sudo] пароль для vadim: 
Попробуйте ещё раз.
[sudo] пароль для vadim: 
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Уже установлен пакет xclip самой новой версии (0.13-3).
Обновлено 0 пакетов, установлено 0 новых пакетов, для удаления отмечено 0 пакетов, и 5 пакетов не обновлено.
vadim@vadim-VirtualBox:~$ alias gsed=sed
vadim@vadim-VirtualBox:~$ alias pbcopy='xclip -selection clipboard'
vadim@vadim-VirtualBox:~$ alias pbpaste='xclip -selection clipboard -o'
vadim@vadim-VirtualBox:~$ cd ${GITHUB_USERNAME}/workspace
vadim@vadim-VirtualBox:~/polenk0/workspace$ pushd .
~/polenk0/workspace ~/polenk0/workspace
vadim@vadim-VirtualBox:~/polenk0/workspace$ git clone git@github.com:polenk0/lab08.git projects/lab09
Клонирование в «projects/lab09»...
remote: Enumerating objects: 96, done.
remote: Counting objects: 100% (96/96), done.
remote: Compressing objects: 100% (53/53), done.
remote: Total 96 (delta 25), reused 87 (delta 21), pack-reused 0
Получение объектов: 100% (96/96), 31.66 КиБ | 341.00 КиБ/с, готово.
Определение изменений: 100% (25/25), готово.
vadim@vadim-VirtualBox:~/polenk0/workspace$ cd projects/lab09
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git remote remove origin
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git remote add origin git@github.com:polenk0/lab09.git
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ gsed -i 's/lab08/lab09/g' README.md
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ sudo $PACKAGE_MANAGER install ${GPG_PACKAGE_NAME}
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Уже установлен пакет gpg самой новой версии (2.4.4-2ubuntu17).
Обновлено 0 пакетов, установлено 0 новых пакетов, для удаления отмечено 0 пакетов, и 5 пакетов не обновлено.
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ gpg --list-secret-keys --keyid-format LONG
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ gpg --full-generate-key
gpg (GnuPG) 2.4.4; Copyright (C) 2024 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Выберите тип ключа:
   (1) RSA and RSA
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
   (9) ECC (sign and encrypt) *default*
  (10) ECC (только для подписи)
  (14) Existing key from card
Ваш выбор? 1
длина ключей RSA может быть от 1024 до 4096.
Какой размер ключа Вам необходим? (3072) 3072
Запрошенный размер ключа - 3072 бит
Выберите срок действия ключа.
         0 = не ограничен
      <n>  = срок действия ключа - n дней
      <n>w = срок действия ключа - n недель
      <n>m = срок действия ключа - n месяцев
      <n>y = срок действия ключа - n лет
Срок действия ключа? (0) 0
Срок действия ключа не ограничен
Все верно? (y/N) y

GnuPG должен составить идентификатор пользователя для идентификации ключа.

Ваше полное имя: polenk0
Адрес электронной почты: gadik13377@gmail.com
Примечание: 
Вы выбрали следующий идентификатор пользователя:
    "polenk0 <gadik13377@gmail.com>"

Сменить (N)Имя, (C)Примечание, (E)Адрес; (O)Принять/(Q)Выход? o
Необходимо получить много случайных чисел. Желательно, чтобы Вы
в процессе генерации выполняли какие-то другие действия (печать
на клавиатуре, движения мыши, обращения к дискам); это даст генератору
случайных чисел больше возможностей получить достаточное количество энтропии.
Необходимо получить много случайных чисел. Желательно, чтобы Вы
в процессе генерации выполняли какие-то другие действия (печать
на клавиатуре, движения мыши, обращения к дискам); это даст генератору
случайных чисел больше возможностей получить достаточное количество энтропии.
gpg: создан каталог '/home/vadim/.gnupg/openpgp-revocs.d'
gpg: сертификат отзыва записан в '/home/vadim/.gnupg/openpgp-revocs.d/173CE87F5F025755D25B15F975A712A13F877CCD.rev'.
открытый и секретный ключи созданы и подписаны.

pub   rsa3072 2024-05-19 [SC]
      173CE87F5F025755D25B15F975A712A13F877CCD
uid                      polenk0 <gadik13377@gmail.com>
sub   rsa3072 2024-05-19 [E]

vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ gpg --list-secret-keys --keyid-format LONG
gpg: проверка таблицы доверия
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: глубина: 0  достоверных:   1  подписанных:   0  доверие: 0-, 0q, 0n, 0m, 0f, 1u
/home/vadim/.gnupg/pubring.kbx
------------------------------
sec   rsa3072/75A712A13F877CCD 2024-05-19 [SC]
      173CE87F5F025755D25B15F975A712A13F877CCD
uid               [  абсолютно ] polenk0 <gadik13377@gmail.com>
ssb   rsa3072/93BF9D7C6637ADCD 2024-05-19 [E]

vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ gpg --list-secret-keys --keyid-format LONG
/home/vadim/.gnupg/pubring.kbx
------------------------------
sec   rsa3072/75A712A13F877CCD 2024-05-19 [SC]
      173CE87F5F025755D25B15F975A712A13F877CCD
uid               [  абсолютно ] polenk0 <gadik13377@gmail.com>
ssb   rsa3072/93BF9D7C6637ADCD 2024-05-19 [E]

vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ gpg -K ${GITHUB_USERNAME}
sec   rsa3072 2024-05-19 [SC]
      173CE87F5F025755D25B15F975A712A13F877CCD
uid         [  абсолютно ] polenk0 <gadik13377@gmail.com>
ssb   rsa3072 2024-05-19 [E]

vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ GPG_KEY_ID=$(gpg --list-secret-keys --keyid-format LONG | grep ssb | tail -1 | awk '{print $2}' | awk -F'/' '{print $2}')
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ GPG_SEC_KEY_ID=$(gpg --list-secret-keys --keyid-format LONG | grep sec | tail -1 | awk '{print $2}' | awk -F'/' '{print $2}')
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ gpg --armor --export ${GPG_KEY_ID} | pbcopy
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ pbpaste
pbpastevadim@vadim-VirtualBox:~/polenk0/workspace/projects/open https://github.com/settings/keys
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ Gtk-Message: 21:59:55.217: Not loading module "atk-bridge": The functionality is provided by GTK natively. Please try to not load it.
git config user.signingkey ${GPG_SEC_KEY_ID}
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git config user.signingkey ${GPG_SEC_KEY_ID}
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git config gpg.program gpg
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ test -r ~/.bash_profile && echo 'export GPG_TTY=$(tty)' >> ~/.bash_profile
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ echo 'export GPG_TTY=$(tty)' >> ~/.profile
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ cmake -H. -B_build -DCPACK_GENERATOR="TGZ"
-- [hunter] Initializing Hunter workspace (a20151e4c0740ee7d0f9994476856d813cdead29)
-- [hunter]   https://github.com/cpp-pm/hunter/archive/v0.25.5.tar.gz
-- [hunter]   -> /home/vadim/.hunter/_Base/Download/Hunter/0.25.5/a20151e
-- The C compiler identification is GNU 13.2.0
-- The CXX compiler identification is GNU 13.2.0
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/gcc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- [hunter] Calculating Toolchain-SHA1
-- [hunter] Calculating Config-SHA1
-- [hunter] HUNTER_ROOT: /home/vadim/.hunter
-- [hunter] [ Hunter-ID: a20151e | Toolchain-ID: c7fd7a9 | Config-ID: 4abab25 ]
-- [hunter] GTEST_ROOT: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Install (ver.: 1.14.0)
-- [hunter] Building GTest
loading initial cache file /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/cache.cmake
loading initial cache file /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/args.cmake
-- The C compiler identification is GNU 13.2.0
-- The CXX compiler identification is GNU 13.2.0
-- Check for working C compiler: /usr/bin/gcc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.2s)
-- Generating done (0.0s)
-- Build files have been written to: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Build
[  6%] Creating directories for 'GTest-Release'
[ 12%] Performing download step (download, verify and extract) for 'GTest-Release'
-- Downloading...
   dst='/home/vadim/.hunter/_Base/Download/GTest/1.14.0/2b28c2a/v1.14.0.tar.gz'
   timeout='none'
   inactivity timeout='none'
-- Using src='https://github.com/google/googletest/archive/v1.14.0.tar.gz'
-- [download 0% complete]
-- [download 1% complete]
-- [download 2% complete]
-- [download 3% complete]
-- [download 4% complete]
-- [download 5% complete]
-- [download 6% complete]
-- [download 7% complete]
-- [download 8% complete]
-- [download 9% complete]
-- [download 10% complete]
-- [download 11% complete]
-- [download 12% complete]
-- [download 15% complete]
-- [download 16% complete]
-- [download 17% complete]
-- [download 18% complete]
-- [download 19% complete]
-- [download 21% complete]
-- [download 22% complete]
-- [download 23% complete]
-- [download 24% complete]
-- [download 25% complete]
-- [download 26% complete]
-- [download 27% complete]
-- [download 28% complete]
-- [download 29% complete]
-- [download 30% complete]
-- [download 31% complete]
-- [download 32% complete]
-- [download 33% complete]
-- [download 34% complete]
-- [download 35% complete]
-- [download 36% complete]
-- [download 38% complete]
-- [download 39% complete]
-- [download 40% complete]
-- [download 41% complete]
-- [download 42% complete]
-- [download 43% complete]
-- [download 45% complete]
-- [download 46% complete]
-- [download 47% complete]
-- [download 48% complete]
-- [download 49% complete]
-- [download 50% complete]
-- [download 51% complete]
-- [download 52% complete]
-- [download 53% complete]
-- [download 54% complete]
-- [download 55% complete]
-- [download 56% complete]
-- [download 57% complete]
-- [download 58% complete]
-- [download 59% complete]
-- [download 60% complete]
-- [download 64% complete]
-- [download 65% complete]
-- [download 66% complete]
-- [download 76% complete]
-- [download 77% complete]
-- [download 78% complete]
-- [download 79% complete]
-- [download 80% complete]
-- [download 100% complete]
-- verifying file...
       file='/home/vadim/.hunter/_Base/Download/GTest/1.14.0/2b28c2a/v1.14.0.tar.gz'
-- Downloading... done
-- extracting...
     src='/home/vadim/.hunter/_Base/Download/GTest/1.14.0/2b28c2a/v1.14.0.tar.gz'
     dst='/home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 18%] No update step for 'GTest-Release'
[ 25%] No patch step for 'GTest-Release'
[ 31%] Performing configure step for 'GTest-Release'
loading initial cache file /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/cache.cmake
loading initial cache file /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/args.cmake
-- The C compiler identification is GNU 13.2.0
-- The CXX compiler identification is GNU 13.2.0
-- Check for working C compiler: /usr/bin/gcc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Found Python3: /usr/bin/python3 (found version "3.12.3") found components: Interpreter 
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE  
-- Configuring done (0.4s)
-- Generating done (0.0s)
-- Build files have been written to: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Build/GTest-Release-prefix/src/GTest-Release-build
[ 37%] Performing build step for 'GTest-Release'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtest.a
[ 25%] Built target gtest
[ 37%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_main.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmock.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_main.a
[100%] Built target gmock_main
[ 43%] Performing install step for 'GTest-Release'
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/libgmock.a
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/libgmock_main.a
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/cmake/GTest/GTestTargets-release.cmake
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-assertion-result.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/libgtest.a
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/libgtest_main.a
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/args.cmake
[ 50%] Completed 'GTest-Release'
[ 50%] Built target GTest-Release
[ 56%] Creating directories for 'GTest-Debug'
[ 62%] Performing download step (download, verify and extract) for 'GTest-Debug'
-- verifying file...
       file='/home/vadim/.hunter/_Base/Download/GTest/1.14.0/2b28c2a/v1.14.0.tar.gz'
-- File already exists and hash match (skip download):
  file='/home/vadim/.hunter/_Base/Download/GTest/1.14.0/2b28c2a/v1.14.0.tar.gz'
  SHA1='2b28c2a3a30d86b1759543ef61fac3c4d69f8c4c'
-- extracting...
     src='/home/vadim/.hunter/_Base/Download/GTest/1.14.0/2b28c2a/v1.14.0.tar.gz'
     dst='/home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 68%] No update step for 'GTest-Debug'
[ 75%] No patch step for 'GTest-Debug'
[ 81%] Performing configure step for 'GTest-Debug'
loading initial cache file /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/cache.cmake
loading initial cache file /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/args.cmake
-- The C compiler identification is GNU 13.2.0
-- The CXX compiler identification is GNU 13.2.0
-- Check for working C compiler: /usr/bin/gcc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Found Python3: /usr/bin/python3 (found version "3.12.3") found components: Interpreter 
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE  
-- Configuring done (0.4s)
-- Generating done (0.0s)
-- Build files have been written to: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Build/GTest-Debug-prefix/src/GTest-Debug-build
[ 87%] Performing build step for 'GTest-Debug'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtestd.a
[ 25%] Built target gtest
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 50%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_maind.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmockd.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_maind.a
[100%] Built target gmock_main
[ 93%] Performing install step for 'GTest-Debug'
-- Up-to-date: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include
-- Up-to-date: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Up-to-date: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Up-to-date: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/libgmockd.a
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/libgmock_maind.a
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/cmake/GTest/GTestTargets-debug.cmake
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include
-- Up-to-date: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-assertion-result.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Up-to-date: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Up-to-date: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/libgtestd.a
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/libgtest_maind.a
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest/args.cmake
[100%] Completed 'GTest-Debug'
[100%] Built target GTest-Debug
-- [hunter] Build step successful (dir: /home/vadim/.hunter/_Base/a20151e/c7fd7a9/4abab25/Build/GTest)
-- [hunter] Cache saved: /home/vadim/.hunter/_Base/Cache/raw/6e08ed6dee4601ebf5f16ae1f6fb0f66e7cb9b28.tar.bz2
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE  
-- Configuring done (31.3s)
-- Generating done (0.0s)
-- Build files have been written to: /home/vadim/polenk0/workspace/projects/lab09/_build
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ cmake --build _build --target package
[ 25%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[ 50%] Linking CXX static library libprint.a
[ 50%] Built target print
[ 75%] Building CXX object CMakeFiles/demo.dir/demo/main.cpp.o
[100%] Linking CXX executable demo
[100%] Built target demo
Run CPack packaging tool...
CPack: Create package using TGZ
CPack: Install projects
CPack: - Run preinstall target for: print
CPack: - Install project: print []
CPack: Create package
CPack: - package: /home/vadim/polenk0/workspace/projects/lab09/_build/print-.1.0.0-Linux.tar.gz generated.
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git tag -s v0.1.0.0
fatal: нет описания метки?
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git tag -v v0.1.0.0
error: метка  «v0.1.0.0» не найдена.
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git tag -s v0.1.0.0
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git tag -v v0.1.0.0
object 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1
type commit
tag v0.1.0.0
tagger polenk0 <gadik13377@gmail.com> 1716145440 +0300

a
gpg: Подпись сделана Вс 19 мая 2024 22:04:18 MSK
gpg:                ключом RSA с идентификатором 173CE87F5F025755D25B15F975A712A13F877CCD
gpg: Действительная подпись пользователя "polenk0 <gadik13377@gmail.com>" [абсолютное]
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git show v0.1.0.0
tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
Author: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 21:44:01 2024 +0300

    a

diff --git a/.travis.yml.swo b/.travis.yml.swo
deleted file mode 100644
index 13c38b5..0000000
--- a/.travis.yml.swo
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
Author: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 21:44:01 2024 +0300

    a

diff --git a/.travis.yml.swo b/.travis.yml.swo
deleted file mode 100644
index 13c38b5..0000000
--- a/.travis.yml.swo
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
Author: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 21:44:01 2024 +0300

    a

diff --git a/.travis.yml.swo b/.travis.yml.swo
deleted file mode 100644
index 13c38b5..0000000
--- a/.travis.yml.swo
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
Author: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 21:44:01 2024 +0300

    a

diff --git a/.travis.yml.swo b/.travis.yml.swo
deleted file mode 100644
index 13c38b5..0000000
--- a/.travis.yml.swo
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
Author: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 21:44:01 2024 +0300

    a

diff --git a/.travis.yml.swo b/.travis.yml.swo
deleted file mode 100644
index 13c38b5..0000000
--- a/.travis.yml.swo
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
Author: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 21:44:01 2024 +0300

    a

diff --git a/.travis.yml.swo b/.travis.yml.swo
deleted file mode 100644
index 13c38b5..0000000
--- a/.travis.yml.swo
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
Author: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 21:44:01 2024 +0300

    a

diff --git a/.travis.yml.swo b/.travis.yml.swo
deleted file mode 100644
index 13c38b5..0000000
--- a/.travis.yml.swo
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
Author: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 21:44:01 2024 +0300

    a

diff --git a/.travis.yml.swo b/.travis.yml.swo
deleted file mode 100644
index 13c38b5..0000000
--- a/.travis.yml.swo
:
































tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
Author: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 21:44:01 2024 +0300

    a

diff --git a/.travis.yml.swo b/.travis.yml.swo
deleted file mode 100644
index 13c38b5..0000000
--- a/.travis.yml.swo
...skipping...

                   SUMMARY OF LESS COMMANDS

      Commands marked with * may be preceded by a number, N.
      Notes in parentheses indicate the behavior if N is given.
      A key preceded by a caret indicates the Ctrl key; thus ^K is ctrl-K.

  h  H                 Display this help.
  q  :q  Q  :Q  ZZ     Exit.
 ---------------------------------------------------------------------------

                           MOVING

  e  ^E  j  ^N  CR  *  Forward  one line   (or N lines).
  y  ^Y  k  ^K  ^P  *  Backward one line   (or N lines).
  f  ^F  ^V  SPACE  *  Forward  one window (or N lines).
  b  ^B  ESC-v      *  Backward one window (or N lines).
  z                 *  Forward  one window (and set window to N).
  w                 *  Backward one window (and set window to N).
  ESC-SPACE         *  Forward  one window, but don't stop at end-of-file.
  d  ^D             *  Forward  one half-window (and set half-window to N).
  u  ^U             *  Backward one half-window (and set half-window to N).
  ESC-)  RightArrow *  Right one half screen width (or N positions).
  ESC-(  LeftArrow  *  Left  one half screen width (or N positions).
  ESC-}  ^RightArrow   Right to last column displayed.
  ESC-{  ^LeftArrow    Left  to first column.
  F                    Forward forever; like "tail -f".

                   SUMMARY OF LESS COMMANDS

      Commands marked with * may be preceded by a number, N.
      Notes in parentheses indicate the behavior if N is given.
      A key preceded by a caret indicates the Ctrl key; thus ^K is ctrl-K.

  h  H                 Display this help.
  q  :q  Q  :Q  ZZ     Exit.
 ---------------------------------------------------------------------------

                           MOVING

  e  ^E  j  ^N  CR  *  Forward  one line   (or N lines).
  y  ^Y  k  ^K  ^P  *  Backward one line   (or N lines).
  f  ^F  ^V  SPACE  *  Forward  one window (or N lines).
  b  ^B  ESC-v      *  Backward one window (or N lines).
  z                 *  Forward  one window (and set window to N).
  w                 *  Backward one window (and set window to N).
  ESC-SPACE         *  Forward  one window, but don't stop at end-of-file.
  d  ^D             *  Forward  one half-window (and set half-window to N).
  u  ^U             *  Backward one half-window (and set half-window to N).
  ESC-)  RightArrow *  Right one half screen width (or N positions).
  ESC-(  LeftArrow  *  Left  one half screen width (or N positions).
  ESC-}  ^RightArrow   Right to last column displayed.
  ESC-{  ^LeftArrow    Left  to first column.
  F                    Forward forever; like "tail -f".
  ESC-F                Like F but stop when search pattern is found.
  r  ^R  ^L            Repaint screen.
  R                    Repaint screen, discarding buffered input.
        ---------------------------------------------------
        Default "window" is the screen height.
        Default "half-window" is half of the screen height.
...skipping...
tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
Author: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 21:44:01 2024 +0300

    a

diff --git a/.travis.yml.swo b/.travis.yml.swo
deleted file mode 100644
index 13c38b5..0000000
--- a/.travis.yml.swo
+++ /dev/null
@@ -1,12 +0,0 @@
-script:
-- cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install -DBUILD_TESTS=ON
-- cmake --build _build
-- cmake --build _build --target install
-- cmake --build _build --target test -- ARGS=--verbose
-addons:
-  apt:
-    sources:
-      - george-edison55-precise-backports
-    packages:
-      - cmake
-      - cmake-data
diff --git a/a b/a
new file mode 100644
index 0000000..8b13789
--- /dev/null
+++ b/a
@@ -0,0 +1 @@
+
...skipping...
commit 3915bc99f76fb1ec239ef5a5d5edfbbc1acbddf1 (HEAD -> main, tag: v0.1.0.0)
tag v0.1.0.0
Tagger: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 22:04:00 2024 +0300

a
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEEFzzof18CV1XSWxX5dacSoT+HfM0FAmZKTTIACgkQdacSoT+H
fM1hwAwAnxvDKfEXTrl18kp8f5ZRXU09aYCj3SlXY5XDJLLniBx+Dd8Y9W9P+RkI
GnssOIJKxakBJXGc2nKfTBFiUYByQHl3sVc4qSz3dDTz1KyrjztjkyOvwSYqSUog
G9J8tShgphrVIdfyDssAZx2kOZt4a85DrlHk2DYcEpLah4/mJx0Ug3jMR5Rh8eOw
eyPLq/fPmbwmnCZiqXQ23crUemO1IXDC1S87RQVKWoJLrHVPfACdWjp7u7jXOJcU
+ggqxlU6BT/awccOJmRfFbfOmo6EqjlUZXdDRrKAzjLWkSutSISvdJpn4kjkZ3vW
3xdx7Rh5wFv3OvjHN6bljYwPVGyq6aUn70XkhNqBX8HRh+pBxYaZ5UFzgNQAv7aA
GQL+wLTr+rllcww/vzYQpX75ARbRmykck2b/BCKxdCWWzJYCjAmNCLcLI2yRRNSm
3Kj05L1OVBqoy5Oy9qLF/EsiUGdjSaYs4Csnl4+nqkoMpLFFeKqoaoEes0St358P
hK5yY5b/
=Fqom
-----END PGP SIGNATURE-----

Author: polenk0 <gadik13377@gmail.com>
Date:   Sun May 19 21:44:01 2024 +0300

    a

diff --git a/.travis.yml.swo b/.travis.yml.swo
deleted file mode 100644
index 13c38b5..0000000
--- a/.travis.yml.swo
+++ /dev/null
@@ -1,12 +0,0 @@
...skipping...

                   SUMMARY OF LESS COMMANDS

      Commands marked with * may be preceded by a number, N.
      Notes in parentheses indicate the behavior if N is given.
      A key preceded by a caret indicates the Ctrl key; thus ^K is ctrl-K.

  h  H                 Display this help.
  q  :q  Q  :Q  ZZ     Exit.
 ---------------------------------------------------------------------------

                           MOVING

  e  ^E  j  ^N  CR  *  Forward  one line   (or N lines).
  y  ^Y  k  ^K  ^P  *  Backward one line   (or N lines).
  f  ^F  ^V  SPACE  *  Forward  one window (or N lines).
  b  ^B  ESC-v      *  Backward one window (or N lines).
  z                 *  Forward  one window (and set window to N).
  w                 *  Backward one window (and set window to N).
  ESC-SPACE         *  Forward  one window, but don't stop at end-of-file.
  d  ^D             *  Forward  one half-window (and set half-window to N).
  u  ^U             *  Backward one half-window (and set half-window to N).
  ESC-)  RightArrow *  Right one half screen width (or N positions).
  ESC-(  LeftArrow  *  Left  one half screen width (or N positions).
  ESC-}  ^RightArrow   Right to last column displayed.
  ESC-{  ^LeftArrow    Left  to first column.
  F                    Forward forever; like "tail -f".
  ESC-F                Like F but stop when search pattern is found.
  r  ^R  ^L            Repaint screen.
  R                    Repaint screen, discarding buffered input.
        ---------------------------------------------------
        Default "window" is the screen height.

                   SUMMARY OF LESS COMMANDS

      Commands marked with * may be preceded by a number, N.
      Notes in parentheses indicate the behavior if N is given.
      A key preceded by a caret indicates the Ctrl key; thus ^K is ctrl-K.

  h  H                 Display this help.
  q  :q  Q  :Q  ZZ     Exit.
 ---------------------------------------------------------------------------

                           MOVING

  e  ^E  j  ^N  CR  *  Forward  one line   (or N lines).
  y  ^Y  k  ^K  ^P  *  Backward one line   (or N lines).
  f  ^F  ^V  SPACE  *  Forward  one window (or N lines).
  b  ^B  ESC-v      *  Backward one window (or N lines).
  z                 *  Forward  one window (and set window to N).
  w                 *  Backward one window (and set window to N).
  ESC-SPACE         *  Forward  one window, but don't stop at end-of-file.
  d  ^D             *  Forward  one half-window (and set half-window to N).
  u  ^U             *  Backward one half-window (and set half-window to N).
  ESC-)  RightArrow *  Right one half screen width (or N positions).
  ESC-(  LeftArrow  *  Left  one half screen width (or N positions).
  ESC-}  ^RightArrow   Right to last column displayed.
  ESC-{  ^LeftArrow    Left  to first column.
  F                    Forward forever; like "tail -f".
  ESC-F                Like F but stop when search pattern is found.
Warning: "e --version" exists; Overwrite, Append, Don't log, or Quit?vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git push origin master --tags
error: src refspec master ничему не соответствует
error: не удалось отправить некоторые ссылки в «github.com:polenk0/lab09.git»
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git push origin main --tags
ERROR: Repository not found.
fatal: Не удалось прочитать из внешнего репозитория.

Удостоверьтесь, что у вас есть необходимые права доступа
и репозиторий существует.
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ git push origin main --tags
Перечисление объектов: 97, готово.
Подсчет объектов: 100% (97/97), готово.
При сжатии изменений используется до 8 потоков
Сжатие объектов: 100% (50/50), готово.
Запись объектов: 100% (97/97), 32.27 КиБ | 32.27 МиБ/с, готово.
Всего 97 (изменений 25), повторно использовано 96 (изменений 25), повторно использовано пакетов 0
remote: Resolving deltas: 100% (25/25), done.
To github.com:polenk0/lab09.git
 * [new branch]      main -> main
 * [new tag]         v0.1.0.0 -> v0.1.0.0
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ gh release create 
? Choose a tag v0.1.0.0
? Title (optional) v0.1.0.0
? Release notes Write using generated notes as template
? Is this a prerelease? No
? Submit? Publish release
https://github.com/polenk0/lab09/releases/tag/v0.1.0.0
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ gh release view
v0.1.0.0
polenk0 released this less than a minute ago

  Full Changelog: https://github.com/polenk0/lab09/commits/v0.1.0.0


View on GitHub: https://github.com/polenk0/lab09/releases/tag/v0.1.0.0
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ mkdir releases
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ gh release download --repo git@github.com:Pavel172/lab09.git --archive zip
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ ls
 a                   DESCRIPTION                     LICENSE
 _build              Dockerfile                      _logs
 ChangeLog.md       'e --version'                    README.md
 cmake               examples                        releases
 CMakeLists.txt     'h origin main --force --tags'   sources
 CPackConfig.cmake   include                         tests
 demo                lab09-0.1.0.0.zip
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ unzip lab09-0.1.0.0.zip 
Archive:  lab09-0.1.0.0.zip
8f4540425c2a4be4ff1c2dfeeb23e2028373453b
   creating: lab09-0.1.0.0/
  inflating: lab09-0.1.0.0/.gitignore  
  inflating: lab09-0.1.0.0/.gitmodules  
 extracting: lab09-0.1.0.0/.test.txt  
  inflating: lab09-0.1.0.0/.travis.yml  
  inflating: lab09-0.1.0.0/CMakeLists.txt  
  inflating: lab09-0.1.0.0/CPackConfig.cmake  
 extracting: lab09-0.1.0.0/ChangeLog.md  
 extracting: lab09-0.1.0.0/DESCRIPTION  
  inflating: lab09-0.1.0.0/Dockerfile  
  inflating: lab09-0.1.0.0/LICENSE   
  inflating: lab09-0.1.0.0/README.md  
   creating: lab09-0.1.0.0/_logs/
   creating: lab09-0.1.0.0/_logs/polly/
   creating: lab09-0.1.0.0/_logs/polly/clang-cxx14/
  inflating: lab09-0.1.0.0/_logs/polly/clang-cxx14/log-0.txt  
  inflating: lab09-0.1.0.0/_logs/polly/clang-cxx14/log.txt  
   creating: lab09-0.1.0.0/_logs/polly/default/
  inflating: lab09-0.1.0.0/_logs/polly/default/log-0.txt  
  inflating: lab09-0.1.0.0/_logs/polly/default/log.txt  
   creating: lab09-0.1.0.0/cmake/
  inflating: lab09-0.1.0.0/cmake/HunterGate.cmake  
   creating: lab09-0.1.0.0/demo/
  inflating: lab09-0.1.0.0/demo/main.cpp  
   creating: lab09-0.1.0.0/examples/
  inflating: lab09-0.1.0.0/examples/example1.cpp  
  inflating: lab09-0.1.0.0/examples/example2.cpp  
   creating: lab09-0.1.0.0/include/
  inflating: lab09-0.1.0.0/include/print.hpp  
   creating: lab09-0.1.0.0/sources/
  inflating: lab09-0.1.0.0/sources/print.cpp  
 extracting: lab09-0.1.0.0/test.txt  
   creating: lab09-0.1.0.0/tests/
  inflating: lab09-0.1.0.0/tests/test1.cpp  
   creating: lab09-0.1.0.0/tools/
   creating: lab09-0.1.0.0/tools/polly/
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ rm -r lab09-0.1.0.0.zip
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ ls -a lab09-0.1.0.0/
.                  demo         include    .test.txt
..                 DESCRIPTION  LICENSE    test.txt
ChangeLog.md       Dockerfile   _logs      tools
cmake              examples     README.md  .travis.yml
CMakeLists.txt     .gitignore   sources
CPackConfig.cmake  .gitmodules  tests
vadim@vadim-VirtualBox:~/polenk0/workspace/projects/lab09$ popd
~/polenk0/workspace
vadim@vadim-VirtualBox:~/polenk0/workspace$ export LAB_NUMBER=09
vadim@vadim-VirtualBox:~/polenk0/workspace$ git clone git@github.com:tp-labs/lab09.git tasks/lab${LAB_NUMBER}
Клонирование в «tasks/lab09»...
remote: Enumerating objects: 101, done.
remote: Counting objects: 100% (33/33), done.
remote: Compressing objects: 100% (26/26), done.
remote: Total 101 (delta 9), reused 29 (delta 7), pack-reused 68
Получение объектов: 100% (101/101), 1.18 МиБ | 1.55 МиБ/с, готово.
Определение изменений: 100% (31/31), готово.
vadim@vadim-VirtualBox:~/polenk0/workspace$ mkdir reports/lab${LAB_NUMBER}
vadim@vadim-VirtualBox:~/polenk0/workspace$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
vadim@vadim-VirtualBox:~/polenk0/workspace$ cd reports/lab${LAB_NUMBER}
vadim@vadim-VirtualBox:~/polenk0/workspace/reports/lab09$ edit REPORT.md

[1]+  Остановлен    edit REPORT.md
vadim@vadim-VirtualBox:~/polenk0/workspace/reports/lab09$ gist REPORT.md

```

## Links

- [Create Release](https://help.github.com/articles/creating-releases/)
- [Get GitHub Token](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/)
- [Signing Commits](https://help.github.com/articles/signing-commits-with-gpg/)
- [Go Setup](http://www.golangbootcamp.com/book/get_setup)
- [github-release](https://github.com/aktau/github-release)

```
Copyright (c) 2015-2021 The ISC Authors
```
