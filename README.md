sam@Noutbuk-Samvel ~ % export GITHUB_USERNAME=<имя_пользователя>
zsh: parse error near `\n'
sam@Noutbuk-Samvel ~ % export GITHUB_USERNAME=<имя_пexport GITHUB_USERNAME=<имя_пользователя 
zsh: no such file or directory: имя_пexport
sam@Noutbuk-Samvel ~ % export GITHUB_USERNAME=<имя_пользователя>
sam@Noutbuk-Samvel ~ % clear








































sam@Noutbuk-Samvel ~ % export GITHUB_USERNAME=samchik7          
sam@Noutbuk-Samvel ~ % alias gsed=sed
sam@Noutbuk-Samvel ~ % cd ${GITHUB_USERNAME}/workspace
sam@Noutbuk-Samvel workspace % pushd .
~/samchik7/workspace ~/samchik7/workspace
sam@Noutbuk-Samvel workspace % source scripts/activate
sam@Noutbuk-Samvel workspace % git clone https://github.com/${GITHUB_USERNAME}/lab06 projects/lab07
Cloning into 'projects/lab07'...
remote: Enumerating objects: 145, done.
remote: Counting objects: 100% (145/145), done.
remote: Compressing objects: 100% (80/80), done.
remote: Total 145 (delta 45), reused 140 (delta 43), pack-reused 0 (from 0)
Receiving objects: 100% (145/145), 362.88 KiB | 1.28 MiB/s, done.
Resolving deltas: 100% (45/45), done.
sam@Noutbuk-Samvel workspace % cd projects/lab07
sam@Noutbuk-Samvel lab07 % git remote remove origin
sam@Noutbuk-Samvel lab07 % git remote add origin https://github.com/${GITHUB_USERNAME}/lab07
sam@Noutbuk-Samvel lab07 % mkdir -p cmake
sam@Noutbuk-Samvel lab07 % wget https://raw.githubusercontent.com/cpp-pm/gate/master/cmake/HunterGate.cmake -O cmake/HunterGate.cmake
--2025-05-15 10:08:26--  https://raw.githubusercontent.com/cpp-pm/gate/master/cmake/HunterGate.cmake
Распознаётся raw.githubusercontent.com (raw.githubusercontent.com)… 2606:50c0:8000::154, 2606:50c0:8001::154, 2606:50c0:8002::154, ...
Подключение к raw.githubusercontent.com (raw.githubusercontent.com)|2606:50c0:8000::154|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 17231 (17K) [text/plain]
Сохранение в: «cmake/HunterGate.cmake»

cmake/HunterGate.cma 100%[===================>]  16,83K  --.-KB/s    за 0,001s  

2025-05-15 10:08:27 (13,5 MB/s) - «cmake/HunterGate.cmake» сохранён [17231/17231]

sam@Noutbuk-Samvel lab07 % HunterGate(
    URL "https://github.com/cpp-pm/hunter/archive/v0.23.308.tar.gz"
    SHA1 "23f1b5a0acffae50fda423388c843a8e7b6e1eb0"
)
zsh: unknown file attribute: \n
sam@Noutbuk-Samvel lab07 % HunterGate(
    URL "https://github.com/cpp-pm/hunter/archive/v0.23.308.tar.gz"
    SHA1 "23f1b5a0acffae50fda423388c843a8e7b6e1eb0")
zsh: unknown file attribute: \n
sam@Noutbuk-Samvel lab07 % gsed -i '/cmake_minimum_required(VERSION 3.4)/a\

include("cmake/HunterGate.cmake")
quote> HunterGate(
    URL "https://github.com/cpp-pm/hunter/archive/v0.23.308.tar.gz"
    SHA1 "23f1b5a0acffae50fda423388c843a8e7b6e1eb0"
)
quote> ' CMakeLists.txt
sed: 1: "CMakeLists.txt": invalid command code C
sam@Noutbuk-Samvel lab07 % git rm -rf third-party/gtest 
rm 'third-party/gtest/CMakeFiles/CMakeDirectoryInformation.cmake'
rm 'third-party/gtest/CMakeFiles/progress.marks'
rm 'third-party/gtest/CTestTestfile.cmake'
rm 'third-party/gtest/Makefile'
rm 'third-party/gtest/cmake_install.cmake'
rm 'third-party/gtest/googlemock/CMakeFiles/CMakeDirectoryInformation.cmake'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/DependInfo.cmake'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/build.make'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/cmake_clean.cmake'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/cmake_clean_target.cmake'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/compiler_depend.make'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/compiler_depend.ts'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/depend.make'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/flags.make'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/link.txt'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/progress.make'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o.d'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/DependInfo.cmake'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/build.make'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/cmake_clean.cmake'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/cmake_clean_target.cmake'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/compiler_depend.make'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/compiler_depend.ts'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/depend.make'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/flags.make'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/link.txt'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/progress.make'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o'
rm 'third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o.d'
rm 'third-party/gtest/googlemock/CMakeFiles/progress.marks'
rm 'third-party/gtest/googlemock/CTestTestfile.cmake'
rm 'third-party/gtest/googlemock/Makefile'
rm 'third-party/gtest/googlemock/cmake_install.cmake'
rm 'third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/DependInfo.cmake'
rm 'third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/build.make'
rm 'third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/cmake_clean.cmake'
rm 'third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/cmake_clean_target.cmake'
rm 'third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/compiler_depend.make'
rm 'third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/compiler_depend.ts'
rm 'third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/depend.make'
rm 'third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/link.txt'
rm 'third-party/gtest/googlemock/gtest/CMakeFiles/gtest.dir/progress.make'
rm 'third-party/gtest/googlemock/gtest/generated/GTestConfig.cmake'
rm 'third-party/gtest/googlemock/gtest/generated/GTestConfigVersion.cmake'
rm 'third-party/gtest/googlemock/gtest/generated/gmock.pc'
rm 'third-party/gtest/googlemock/gtest/generated/gmock_main.pc'
rm 'third-party/gtest/googlemock/gtest/generated/gtest.pc'
rm 'third-party/gtest/googlemock/gtest/generated/gtest_main.pc'
sam@Noutbuk-Samvel lab07 % gsed -i '/set(PRINT_VERSION_STRING "v\${PRINT_VERSION}")/a\
quote> hunter_add_package(GTest)
find_package(GTest CONFIG REQUIRED)
' CMakeLists.txt
sed: 1: "CMakeLists.txt": invalid command code C
sam@Noutbuk-Samvel lab07 % gsed -i 's/add_subdirectory(third-party/gtest)//'
sed: -I or -i may not be used with stdin
sam@Noutbuk-Samvel lab07 % gsed -i 's/gtest_main/GTest::main/'
sed: -I or -i may not be used with stdin
sam@Noutbuk-Samvel lab07 % cmake -H. -B_builds -DBUILD_TESTS=ON
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- [hunter] Initializing Hunter workspace (23f1b5a0acffae50fda423388c843a8e7b6e1eb0)
-- [hunter]   https://github.com/cpp-pm/hunter/archive/v0.23.308.tar.gz
-- [hunter]   -> /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a
CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_private_data.cmake:12 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:35 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_initialize.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:36 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- [hunter] Calculating Toolchain-SHA1
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- [hunter] Calculating Config-SHA1
-- [hunter] HUNTER_ROOT: /Users/sam/.hunter
-- [hunter] [ Hunter-ID: 23f1b5a | Toolchain-ID: 38776ca | Config-ID: 302e72f ]
CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:6 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:4 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.
Call Stack (most recent call first):
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


-- [hunter] GTEST_ROOT: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Install (ver.: 1.11.0)
-- [hunter] Building GTest
loading initial cache file /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/cache.cmake
loading initial cache file /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/args.cmake
CMake Deprecation Warning at CMakeLists.txt:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Check for working C compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
CMake Warning (dev) at /Users/sam/.brew/share/cmake/Modules/ExternalProject/shared_internal_commands.cmake:1276 (message):
  The DOWNLOAD_EXTRACT_TIMESTAMP option was not given and policy CMP0135 is
  not set.  The policy's OLD behavior will be used.  When using a URL
  download, the timestamps of extracted files should preferably be that of
  the time of extraction, otherwise code that depends on the extracted
  contents might not be rebuilt if the URL changes.  The OLD behavior
  preserves the timestamps from the archive instead, but this is usually not
  what you want.  Update your project to the NEW behavior or specify the
  DOWNLOAD_EXTRACT_TIMESTAMP option with a value of true to avoid this
  robustness issue.
Call Stack (most recent call first):
  /Users/sam/.brew/share/cmake/Modules/ExternalProject.cmake:3041 (_ep_add_download_command)
  CMakeLists.txt:152 (ExternalProject_Add)
This warning is for project developers.  Use -Wno-dev to suppress it.

CMake Warning (dev) at /Users/sam/.brew/share/cmake/Modules/ExternalProject/shared_internal_commands.cmake:1276 (message):
  The DOWNLOAD_EXTRACT_TIMESTAMP option was not given and policy CMP0135 is
  not set.  The policy's OLD behavior will be used.  When using a URL
  download, the timestamps of extracted files should preferably be that of
  the time of extraction, otherwise code that depends on the extracted
  contents might not be rebuilt if the URL changes.  The OLD behavior
  preserves the timestamps from the archive instead, but this is usually not
  what you want.  Update your project to the NEW behavior or specify the
  DOWNLOAD_EXTRACT_TIMESTAMP option with a value of true to avoid this
  robustness issue.
Call Stack (most recent call first):
  /Users/sam/.brew/share/cmake/Modules/ExternalProject.cmake:3041 (_ep_add_download_command)
  CMakeLists.txt:152 (ExternalProject_Add)
This warning is for project developers.  Use -Wno-dev to suppress it.

-- Configuring done (0.5s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Build
[  6%] Creating directories for 'GTest-Release'
[ 12%] Performing download step (download, verify and extract) for 'GTest-Release'
-- Downloading...
   dst='/Users/sam/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
   timeout='none'
   inactivity timeout='none'
-- Using src='https://github.com/google/googletest/archive/release-1.11.0.tar.gz'
-- [download 0% complete]
-- [download 1% complete]
-- [download 2% complete]
-- [download 4% complete]
-- [download 5% complete]
-- [download 6% complete]
-- [download 7% complete]
-- [download 8% complete]
-- [download 9% complete]
-- [download 10% complete]
-- [download 11% complete]
-- [download 12% complete]
-- [download 13% complete]
-- [download 15% complete]
-- [download 17% complete]
-- [download 18% complete]
-- [download 19% complete]
-- [download 21% complete]
-- [download 22% complete]
-- [download 24% complete]
-- [download 25% complete]
-- [download 26% complete]
-- [download 27% complete]
-- [download 29% complete]
-- [download 31% complete]
-- [download 32% complete]
-- [download 34% complete]
-- [download 35% complete]
-- [download 37% complete]
-- [download 39% complete]
-- [download 41% complete]
-- [download 43% complete]
-- [download 44% complete]
-- [download 46% complete]
-- [download 47% complete]
-- [download 49% complete]
-- [download 51% complete]
-- [download 52% complete]
-- [download 54% complete]
-- [download 56% complete]
-- [download 58% complete]
-- [download 60% complete]
-- [download 61% complete]
-- [download 63% complete]
-- [download 65% complete]
-- [download 66% complete]
-- [download 68% complete]
-- [download 69% complete]
-- [download 71% complete]
-- [download 73% complete]
-- [download 74% complete]
-- [download 76% complete]
-- [download 78% complete]
-- [download 79% complete]
-- [download 81% complete]
-- [download 83% complete]
-- [download 84% complete]
-- [download 86% complete]
-- [download 88% complete]
-- [download 89% complete]
-- [download 91% complete]
-- [download 93% complete]
-- [download 94% complete]
-- [download 96% complete]
-- [download 98% complete]
-- [download 99% complete]
-- [download 100% complete]
-- verifying file...
       file='/Users/sam/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
-- Downloading... done
-- extracting...
     src='/Users/sam/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
     dst='/Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 18%] No update step for 'GTest-Release'
[ 25%] No patch step for 'GTest-Release'
[ 31%] Performing configure step for 'GTest-Release'
loading initial cache file /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/cache.cmake
loading initial cache file /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/args.cmake
CMake Deprecation Warning at CMakeLists.txt:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Check for working C compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
CMake Deprecation Warning at googlemock/CMakeLists.txt:45 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


CMake Deprecation Warning at googletest/CMakeLists.txt:56 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- Found Python: /Library/Frameworks/Python.framework/Versions/3.12/bin/python3.12 (found version "3.12.5") found components: Interpreter
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (4.5s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Build/GTest-Release-prefix/src/GTest-Release-build
[ 37%] Performing build step for 'GTest-Release'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtest.a
[ 25%] Built target gtest
[ 50%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_main.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmock.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_main.a
[100%] Built target gmock_main
[ 43%] Performing install step for 'GTest-Release'
[ 25%] Built target gtest
[ 50%] Built target gmock
[ 75%] Built target gmock_main
[100%] Built target gtest_main
Install the project...
-- Install configuration: "Release"
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/libgmock.a
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/libgmock_main.a
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/cmake/GTest/GTestTargets-release.cmake
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/libgtest.a
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/libgtest_main.a
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/args.cmake
CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/scripts/try-copy-license.cmake:5 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


[ 50%] Completed 'GTest-Release'
[ 50%] Built target GTest-Release
[ 56%] Creating directories for 'GTest-Debug'
[ 62%] Performing download step (download, verify and extract) for 'GTest-Debug'
-- verifying file...
       file='/Users/sam/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
-- File already exists and hash match (skip download):
  file='/Users/sam/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
  SHA1='7b100bb68db8df1060e178c495f3cbe941c9b058'
-- extracting...
     src='/Users/sam/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
     dst='/Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 68%] No update step for 'GTest-Debug'
[ 75%] No patch step for 'GTest-Debug'
[ 81%] Performing configure step for 'GTest-Debug'
loading initial cache file /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/cache.cmake
loading initial cache file /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/args.cmake
CMake Deprecation Warning at CMakeLists.txt:4 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Check for working C compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
CMake Deprecation Warning at googlemock/CMakeLists.txt:45 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


CMake Deprecation Warning at googletest/CMakeLists.txt:56 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- Found Python: /Library/Frameworks/Python.framework/Versions/3.12/bin/python3.12 (found version "3.12.5") found components: Interpreter
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (2.0s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Build/GTest-Debug-prefix/src/GTest-Debug-build
[ 87%] Performing build step for 'GTest-Debug'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtestd.a
[ 25%] Built target gtest
[ 50%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_maind.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmockd.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_maind.a
[100%] Built target gmock_main
[ 93%] Performing install step for 'GTest-Debug'
[ 25%] Built target gtest
[ 50%] Built target gmock
[ 75%] Built target gmock_main
[100%] Built target gtest_main
Install the project...
-- Install configuration: "Debug"
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/custom
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/libgmockd.a
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/libgmock_maind.a
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/cmake/GTest/GTestTargets-debug.cmake
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-spi.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/custom
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-message.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest_prod.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest.h
-- Up-to-date: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/libgtestd.a
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/libgtest_maind.a
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest/args.cmake
CMake Deprecation Warning at /Users/sam/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/scripts/try-copy-license.cmake:5 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


[100%] Completed 'GTest-Debug'
[100%] Built target GTest-Debug
-- [hunter] Build step successful (dir: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Build/GTest)
-- [hunter] Cache saved: /Users/sam/.hunter/_Base/Cache/raw/37ade9b97bd4b739234db5c4fd9dc99e9ee4d0b1.tar.bz2
-- Found GTest: /Users/sam/.hunter/_Base/23f1b5a/38776ca/302e72f/Install/lib/cmake/GTest/GTestConfig.cmake (found version "1.11.0")
-- Configuring done (34.3s)
CMake Error at CMakeLists.txt:64 (add_executable):
  Cannot find source file:

    /Users/sam/samchik7/workspace/projects/lab07/demo/main.cpp

  Tried extensions .c .C .c++ .cc .cpp .cxx .cu .mpp .m .M .mm .ixx .cppm
  .ccm .cxxm .c++m .h .hh .h++ .hm .hpp .hxx .in .txx .f .F .for .f77 .f90
  .f95 .f03 .hip .ispc


CMake Error at CMakeLists.txt:59 (add_executable):
  No SOURCES given to target: check


CMake Error at CMakeLists.txt:64 (add_executable):
  No SOURCES given to target: demo


CMake Generate step failed.  Build files cannot be regenerated correctly.
sam@Noutbuk-Samvel lab07 % cmake --build _builds
make: Makefile: No such file or directory
make: *** No rule to make target `Makefile'.  Stop.
sam@Noutbuk-Samvel lab07 % cmake --build _builds --target test

make: Makefile: No such file or directory
make: *** No rule to make target `Makefile'.  Stop.
sam@Noutbuk-Samvel lab07 % cmake --build _builds --target test
$ ls -la $HOME/.hunter

make: Makefile: No such file or directory
make: *** No rule to make target `Makefile'.  Stop.
zsh: command not found: $
sam@Noutbuk-Samvel lab07 % cmake --build _builds --target test
make: Makefile: No such file or directory
make: *** No rule to make target `Makefile'.  Stop.
sam@Noutbuk-Samvel lab07 % ls -la $HOME/.hunter
total 0
drwxr-xr-x   6 sam  staff   192 15 май 10:11 _Base
drwxr-xr-x   3 sam  staff    96 15 май 10:10 .
drwxr-x---+ 66 sam  staff  2112 15 май 10:10 ..
sam@Noutbuk-Samvel lab07 % git clone https://github.com/cpp-pm/hunter $HOME/projects/hunter
fatal: destination path '/Users/sam/projects/hunter' already exists and is not an empty directory.
sam@Noutbuk-Samvel lab07 % export HUNTER_ROOT=$HOME/projects/hunter
sam@Noutbuk-Samvel lab07 % rm -rf _builds
sam@Noutbuk-Samvel lab07 % cmake -H. -B_builds -DBUILD_TESTS=ON
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- [hunter] Calculating Toolchain-SHA1
-- [hunter] Calculating Config-SHA1
-- [hunter] HUNTER_ROOT: /Users/sam/projects/hunter
-- [hunter] [ Hunter-ID: xxxxxxx | Toolchain-ID: 38776ca | Config-ID: 0b4a22b ]
-- [hunter] GTEST_ROOT: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Install (ver.: 1.15.2)
-- [hunter] Building GTest
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/cache.cmake
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/args.cmake
-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Check for working C compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.5s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Build
[  6%] Creating directories for 'GTest-Release'
[ 12%] Performing download step (download, verify and extract) for 'GTest-Release'
-- Downloading...
   dst='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
   timeout='none'
   inactivity timeout='none'
-- Using src='https://github.com/google/googletest/archive/v1.15.2.tar.gz'
-- [download 1% complete]
-- [download 3% complete]
-- [download 5% complete]
-- [download 7% complete]
-- [download 9% complete]
-- [download 10% complete]
-- [download 11% complete]
-- [download 13% complete]
-- [download 15% complete]
-- [download 17% complete]
-- [download 18% complete]
-- [download 19% complete]
-- [download 21% complete]
-- [download 23% complete]
-- [download 24% complete]
-- [download 25% complete]
-- [download 27% complete]
-- [download 28% complete]
-- [download 30% complete]
-- [download 31% complete]
-- [download 32% complete]
-- [download 34% complete]
-- [download 35% complete]
-- [download 37% complete]
-- [download 38% complete]
-- [download 40% complete]
-- [download 42% complete]
-- [download 43% complete]
-- [download 44% complete]
-- [download 46% complete]
-- [download 47% complete]
-- [download 48% complete]
-- [download 49% complete]
-- [download 50% complete]
-- [download 51% complete]
-- [download 52% complete]
-- [download 54% complete]
-- [download 56% complete]
-- [download 57% complete]
-- [download 59% complete]
-- [download 61% complete]
-- [download 62% complete]
-- [download 64% complete]
-- [download 65% complete]
-- [download 66% complete]
-- [download 68% complete]
-- [download 70% complete]
-- [download 71% complete]
-- [download 73% complete]
-- [download 75% complete]
-- [download 76% complete]
-- [download 77% complete]
-- [download 79% complete]
-- [download 81% complete]
-- [download 83% complete]
-- [download 85% complete]
-- [download 86% complete]
-- [download 88% complete]
-- [download 89% complete]
-- [download 91% complete]
-- [download 93% complete]
-- [download 94% complete]
-- [download 95% complete]
-- [download 97% complete]
-- [download 98% complete]
-- [download 100% complete]
-- verifying file...
       file='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
-- Downloading... done
-- extracting...
     src='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
     dst='/Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 18%] No update step for 'GTest-Release'
[ 25%] No patch step for 'GTest-Release'
[ 31%] Performing configure step for 'GTest-Release'
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/cache.cmake
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/args.cmake
-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Check for working C compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (0.8s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Build/GTest-Release-prefix/src/GTest-Release-build
[ 37%] Performing build step for 'GTest-Release'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtest.a
[ 25%] Built target gtest
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 50%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_main.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmock.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_main.a
[100%] Built target gmock_main
[ 43%] Performing install step for 'GTest-Release'
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/libgmock.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/libgmock_main.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestTargets-release.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-assertion-result.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/libgtest.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/libgtest_main.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/args.cmake
[ 50%] Completed 'GTest-Release'
[ 50%] Built target GTest-Release
[ 56%] Creating directories for 'GTest-Debug'
[ 62%] Performing download step (download, verify and extract) for 'GTest-Debug'
-- verifying file...
       file='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
-- File already exists and hash match (skip download):
  file='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
  SHA1='568d58e26bd4e838449ca7ab8ebc152b3cbd210d'
-- extracting...
     src='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
     dst='/Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 68%] No update step for 'GTest-Debug'
[ 75%] No patch step for 'GTest-Debug'
[ 81%] Performing configure step for 'GTest-Debug'
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/cache.cmake
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/args.cmake
-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Check for working C compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (0.8s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Build/GTest-Debug-prefix/src/GTest-Debug-build
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
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/libgmockd.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/libgmock_maind.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestTargets-debug.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-assertion-result.h
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/libgtestd.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/libgtest_maind.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest/args.cmake
[100%] Completed 'GTest-Debug'
[100%] Built target GTest-Debug
-- [hunter] Build step successful (dir: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Build/GTest)
-- [hunter] Cache saved: /Users/sam/projects/hunter/_Base/Cache/raw/b81bd61effb0a147754587fe475b7c919f953998.tar.bz2
-- Found GTest: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Install/lib/cmake/GTest/GTestConfig.cmake (found version "1.15.2")
-- Configuring done (26.5s)
CMake Error at CMakeLists.txt:64 (add_executable):
  Cannot find source file:

    /Users/sam/samchik7/workspace/projects/lab07/demo/main.cpp

  Tried extensions .c .C .c++ .cc .cpp .cxx .cu .mpp .m .M .mm .ixx .cppm
  .ccm .cxxm .c++m .h .hh .h++ .hm .hpp .hxx .in .txx .f .F .for .f77 .f90
  .f95 .f03 .hip .ispc


CMake Error at CMakeLists.txt:59 (add_executable):
  No SOURCES given to target: check


CMake Error at CMakeLists.txt:64 (add_executable):
  No SOURCES given to target: demo


CMake Generate step failed.  Build files cannot be regenerated correctly.
sam@Noutbuk-Samvel lab07 % cmake --build _builds
make: Makefile: No such file or directory
make: *** No rule to make target `Makefile'.  Stop.
sam@Noutbuk-Samvel lab07 % cmake --build _builds --target test
make: Makefile: No such file or directory
make: *** No rule to make target `Makefile'.  Stop.
sam@Noutbuk-Samvel lab07 % cat $HUNTER_ROOT/cmake/configs/default.cmake | grep GTest
  hunter_default_version(GTest VERSION 1.7.0-hunter-6)
  hunter_default_version(GTest VERSION 1.15.2)
sam@Noutbuk-Samvel lab07 % cat $HUNTER_ROOT/cmake/projects/GTest/hunter.cmake
# Copyright (c) 2013, Ruslan Baratov
# All rights reserved.

# !!! DO NOT PLACE HEADER GUARDS HERE !!!

include(hunter_add_version)
include(hunter_cacheable)
include(hunter_download)
include(hunter_pick_scheme)
include(hunter_cmake_args)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter.tar.gz"
    SHA1
    1ed1c26d11fb592056c1cb912bd3c784afa96eaa
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-1"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-1.tar.gz"
    SHA1
    0cb1dcf75e144ad052d3f1e4923a7773bf9b494f
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-2"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-2.tar.gz"
    SHA1
    e62b2ef70308f63c32c560f7b6e252442eed4d57
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-3"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-3.tar.gz"
    SHA1
    fea7d3020e20f059255484c69755753ccadf6362
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-4"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-4.tar.gz"
    SHA1
    9b439c0c25437a083957b197ac6905662a5d901b
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-5"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-5.tar.gz"
    SHA1
    796804df3facb074087a4d8ba6f652e5ac69ad7f
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-6"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-6.tar.gz"
    SHA1
    64b93147abe287da8fe4e18cfd54ba9297dafb82
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-7"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-7.tar.gz"
    SHA1
    19b5c98747768bcd0622714f2ed40f17aee406b2
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-8"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-8.tar.gz"
    SHA1
    ac4d2215aa1b1d745a096e5e3b2dbe0c0f229ea5
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-9"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-9.tar.gz"
    SHA1
    8a47fe9c4e550f4ed0e2c05388dd291a059223d9
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-10"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-10.tar.gz"
    SHA1
    374e6dbe8619ab467c6b1a0b470a598407b172e9
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-11"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-11.tar.gz"
    SHA1
    c6ae948ca2bea1d734af01b1069491b00933ed31
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p2
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p2.tar.gz"
    SHA1
    93148cb8850abe78b76ed87158fdb6b9c48e38c4
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p5
    URL https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p5.tar.gz
    SHA1 3325aa4fc8b30e665c9f73a60f19387b7db36f85
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p6
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p6.tar.gz"
    SHA1
    f57096bd01c6f8cbef043b312d4d1e82f29648b6
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p7
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p7.tar.gz"
    SHA1
    4fe083a96d7597f7dce6f453dca01e1d94a1e45b
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p8
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p8.tar.gz"
    SHA1
    1cdd396b20c8d29f7ea08baaa49673b1c261f545
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p9
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p9.tar.gz"
    SHA1
    a345f16cb610e0b5dfa7778dc2852b784cfede5b
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p10
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p10.tar.gz"
    SHA1
    1d92c9f51af756410843b13f8c4e4df09e235394
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.8.0-hunter-p11"
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p11.tar.gz"
    SHA1
    76c6aec038f7d7258bf5c4f45c4817b34039d285
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.8.1"
    URL
    "https://github.com/google/googletest/archive/release-1.8.1.tar.gz"
    SHA1
    152b849610d91a9dfa1401293f43230c2e0c33f8
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.10.0"
    URL
    "https://github.com/google/googletest/archive/release-1.10.0.tar.gz"
    SHA1
    9c89be7df9c5e8cb0bc20b3c4b39bf7e82686770
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.10.0-p0"
    URL
    "https://github.com/hunter-packages/googletest/archive/v1.10.0-p0.tar.gz"
    SHA1
    f7c72be12120e018f53cda0e0daa26fab5da7dfc
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.10.0-p1"
    URL
    "https://github.com/hunter-packages/googletest/archive/v1.10.0-p1.tar.gz"
    SHA1
    06a1f667f200ff94d38b608e44c3c8061c7b8f2f
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.11.0"
    URL
    "https://github.com/google/googletest/archive/release-1.11.0.tar.gz"
    SHA1
    7b100bb68db8df1060e178c495f3cbe941c9b058
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.12.1"
    URL
    "https://github.com/google/googletest/archive/release-1.12.1.tar.gz"
    SHA1
    cdddd449d4e3aa7bd421d4519c17139ea1890fe7
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.13.0"
    URL
    "https://github.com/google/googletest/archive/v1.13.0.tar.gz"
    SHA1
    bfa4b5131b6eaac06962c251742c96aab3f7aa78
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.14.0"
    URL
    "https://github.com/google/googletest/archive/v1.14.0.tar.gz"
    SHA1
    2b28c2a3a30d86b1759543ef61fac3c4d69f8c4c
)

hunter_add_version(
        PACKAGE_NAME
        GTest
        VERSION
        "1.15.2"
        URL
        "https://github.com/google/googletest/archive/v1.15.2.tar.gz"
        SHA1
        568d58e26bd4e838449ca7ab8ebc152b3cbd210d
)


if(HUNTER_GTest_VERSION VERSION_LESS 1.8.0 OR HUNTER_GTest_VERSION VERSION_GREATER_EQUAL 1.11.0)
  set(_gtest_license "LICENSE")
else()
  set(_gtest_license "googletest/LICENSE")
endif()

# gtest_force_shared_crt prevents GoogleTest from modifying options
# rather than forcing it to use shared libraries
hunter_cmake_args(
    GTest
    CMAKE_ARGS
    HUNTER_INSTALL_LICENSE_FILES=${_gtest_license}
    gtest_force_shared_crt=TRUE
)

hunter_pick_scheme(DEFAULT url_sha1_cmake)
hunter_cacheable(GTest)
hunter_download(PACKAGE_NAME GTest PACKAGE_INTERNAL_DEPS_ID 1)
sam@Noutbuk-Samvel lab07 %  mkdir cmake/Hunter
sam@Noutbuk-Samvel lab07 % cat > cmake/Hunter/config.cmake <<EOF
hunter_config(GTest VERSION 1.7.0-hunter-9)
EOF
sam@Noutbuk-Samvel lab07 % mkdir demo
sam@Noutbuk-Samvel lab07 % cat > demo/main.cpp <<EOF
#include <print.hpp>

#include <cstdlib>

int main(int argc, char* argv[])
{
  const char* log_path = std::getenv("LOG_PATH");
  if (log_path == nullptr)
  {
    std::cerr << "undefined environment variable: LOG_PATH" << std::endl;
    return 1;
  }
  std::string text;
  while (std::cin >> text)
  {
    std::ofstream out{log_path, std::ios_base::app};
    print(text, out);
    out << std::endl;
  }
}
EOF
sam@Noutbuk-Samvel lab07 % gsed -i '/endif()/a\

add_executable(demo ${CMAKE_CURRENT_SOURCE_DIR}/demo/main.cpp)
target_link_libraries(demo print)
install(TARGETS demo RUNTIME DESTINATION bin)
' CMakeLists.txt
sed: 1: "CMakeLists.txt": invalid command code C
sam@Noutbuk-Samvel lab07 % mkdir tools
sam@Noutbuk-Samvel lab07 % git submodule add https://github.com/ruslo/polly tools/polly
Cloning into '/Users/sam/samchik7/workspace/projects/lab07/tools/polly'...
remote: Enumerating objects: 6578, done.
remote: Counting objects: 100% (32/32), done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 6578 (delta 21), reused 20 (delta 17), pack-reused 6546 (from 1)
Receiving objects: 100% (6578/6578), 1.68 MiB | 5.02 MiB/s, done.
Resolving deltas: 100% (4551/4551), done.
sam@Noutbuk-Samvel lab07 % tools/polly/bin/polly.py --test
Python version: 3.12
Build dir: /Users/sam/samchik7/workspace/projects/lab07/_builds/default
Execute command: [
  `which`
  `cmake`
]

[/Users/sam/samchik7/workspace/projects/lab07]> "which" "cmake"

/Users/sam/.brew/bin/cmake
Execute command: [
  `cmake`
  `--version`
]

[/Users/sam/samchik7/workspace/projects/lab07]> "cmake" "--version"

cmake version 3.31.6

CMake suite maintained and supported by Kitware (kitware.com/cmake).
Execute command: [
  `cmake`
  `-H.`
  `-B/Users/sam/samchik7/workspace/projects/lab07/_builds/default`
  `-DCMAKE_TOOLCHAIN_FILE=/Users/sam/samchik7/workspace/projects/lab07/tools/polly/default.cmake`
]

[/Users/sam/samchik7/workspace/projects/lab07]> "cmake" "-H." "-B/Users/sam/samchik7/workspace/projects/lab07/_builds/default" "-DCMAKE_TOOLCHAIN_FILE=/Users/sam/samchik7/workspace/projects/lab07/tools/polly/default.cmake"

CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- [polly] Used toolchain: Default
-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- [hunter] Calculating Toolchain-SHA1
-- [hunter] Calculating Config-SHA1
-- [hunter] HUNTER_ROOT: /Users/sam/projects/hunter
-- [hunter] [ Hunter-ID: xxxxxxx | Toolchain-ID: 38776ca | Config-ID: 0b4a22b ]
-- [hunter] GTEST_ROOT: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Install (ver.: 1.15.2)
-- Found GTest: /Users/sam/projects/hunter/_Base/xxxxxxx/38776ca/0b4a22b/Install/lib/cmake/GTest/GTestConfig.cmake (found version "1.15.2")
-- Configuring done (3.7s)
-- Generating done (0.1s)
-- Build files have been written to: /Users/sam/samchik7/workspace/projects/lab07/_builds/default
Execute command: [
  `cmake`
  `--build`
  `/Users/sam/samchik7/workspace/projects/lab07/_builds/default`
  `--`
]

[/Users/sam/samchik7/workspace/projects/lab07]> "cmake" "--build" "/Users/sam/samchik7/workspace/projects/lab07/_builds/default" "--"

[ 25%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[ 50%] Linking CXX static library libprint.a
[ 50%] Built target print
[ 75%] Building CXX object CMakeFiles/demo.dir/demo/main.cpp.o
[100%] Linking CXX executable demo
[100%] Built target demo
Run tests
Execute command: [
  `ctest`
]

[/Users/sam/samchik7/workspace/projects/lab07/_builds/default]> "ctest"

*********************************
No test configuration file found!
*********************************
Usage

  ctest [options]

-
Log saved: /Users/sam/samchik7/workspace/projects/lab07/_logs/polly/default/log.txt
-
Generate: 0:00:04.838237s
Build: 0:00:02.692349s
Test: 0:00:00.153792s
-
Total: 0:00:07.685890s
-
SUCCESS
sam@Noutbuk-Samvel lab07 % tools/polly/bin/polly.py --install
Python version: 3.12
Build dir: /Users/sam/samchik7/workspace/projects/lab07/_builds/default
Execute command: [
  `which`
  `cmake`
]

[/Users/sam/samchik7/workspace/projects/lab07]> "which" "cmake"

/Users/sam/.brew/bin/cmake
Execute command: [
  `cmake`
  `--version`
]

[/Users/sam/samchik7/workspace/projects/lab07]> "cmake" "--version"

cmake version 3.31.6

CMake suite maintained and supported by Kitware (kitware.com/cmake).

== WARNING ==

Looks like cmake arguments changed. You have two options to fix it:
  * Remove build directory completely by adding '--clear' (works 100%)
  * Run configure again by adding '--reconfig' (you must understand how CMake cache variables works/updated)

- "cmake" "-H." "-B/Users/sam/samchik7/workspace/projects/lab07/_builds/default" "-DCMAKE_TOOLCHAIN_FILE=/Users/sam/samchik7/workspace/projects/lab07/tools/polly/default.cmake"
+ "cmake" "-H." "-B/Users/sam/samchik7/workspace/projects/lab07/_builds/default" "-DCMAKE_TOOLCHAIN_FILE=/Users/sam/samchik7/workspace/projects/lab07/tools/polly/default.cmake" "-DCMAKE_INSTALL_PREFIX=/Users/sam/samchik7/workspace/projects/lab07/_install/default"
?                                                                                                                                                                               +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

sam@Noutbuk-Samvel lab07 %      tools/polly/bin/polly.py --toolchain clang-cxx14
Python version: 3.12
Build dir: /Users/sam/samchik7/workspace/projects/lab07/_builds/clang-cxx14
Execute command: [
  `which`
  `cmake`
]

[/Users/sam/samchik7/workspace/projects/lab07]> "which" "cmake"

/Users/sam/.brew/bin/cmake
Execute command: [
  `cmake`
  `--version`
]

[/Users/sam/samchik7/workspace/projects/lab07]> "cmake" "--version"

cmake version 3.31.6

CMake suite maintained and supported by Kitware (kitware.com/cmake).
Execute command: [
  `cmake`
  `-H.`
  `-B/Users/sam/samchik7/workspace/projects/lab07/_builds/clang-cxx14`
  `-GUnix Makefiles`
  `-DCMAKE_TOOLCHAIN_FILE=/Users/sam/samchik7/workspace/projects/lab07/tools/polly/clang-cxx14.cmake`
]

[/Users/sam/samchik7/workspace/projects/lab07]> "cmake" "-H." "-B/Users/sam/samchik7/workspace/projects/lab07/_builds/clang-cxx14" "-GUnix Makefiles" "-DCMAKE_TOOLCHAIN_FILE=/Users/sam/samchik7/workspace/projects/lab07/tools/polly/clang-cxx14.cmake"

CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.10 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
  to tell CMake that the project requires at least <min> but has been updated
  to work with policies introduced by <max> or earlier.


-- [polly] Used toolchain: clang / c++14 support
-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/clang - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/clang++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- [hunter] Calculating Toolchain-SHA1
-- [hunter] Calculating Config-SHA1
-- [hunter] HUNTER_ROOT: /Users/sam/projects/hunter
-- [hunter] [ Hunter-ID: xxxxxxx | Toolchain-ID: 858098f | Config-ID: 0b4a22b ]
-- [hunter] GTEST_ROOT: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Install (ver.: 1.15.2)
-- [hunter] Building GTest
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/cache.cmake
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/args.cmake
-- [polly] Used toolchain: clang / c++14 support
-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Check for working C compiler: /usr/bin/clang - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/clang++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.4s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Build
[  6%] Creating directories for 'GTest-Release'
[ 12%] Performing download step (download, verify and extract) for 'GTest-Release'
-- verifying file...
       file='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
-- File already exists and hash match (skip download):
  file='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
  SHA1='568d58e26bd4e838449ca7ab8ebc152b3cbd210d'
-- extracting...
     src='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
     dst='/Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 18%] No update step for 'GTest-Release'
[ 25%] No patch step for 'GTest-Release'
[ 31%] Performing configure step for 'GTest-Release'
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/cache.cmake
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/args.cmake
-- [polly] Used toolchain: clang / c++14 support
-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Check for working C compiler: /usr/bin/clang - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/clang++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (0.8s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Build/GTest-Release-prefix/src/GTest-Release-build
[ 37%] Performing build step for 'GTest-Release'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtest.a
[ 25%] Built target gtest
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 50%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_main.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmock.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_main.a
[100%] Built target gmock_main
[ 43%] Performing install step for 'GTest-Release'
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/libgmock.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/libgmock_main.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestTargets-release.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-assertion-result.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/libgtest.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/libgtest_main.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/args.cmake
[ 50%] Completed 'GTest-Release'
[ 50%] Built target GTest-Release
[ 56%] Creating directories for 'GTest-Debug'
[ 62%] Performing download step (download, verify and extract) for 'GTest-Debug'
-- verifying file...
       file='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
-- File already exists and hash match (skip download):
  file='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
  SHA1='568d58e26bd4e838449ca7ab8ebc152b3cbd210d'
-- extracting...
     src='/Users/sam/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
     dst='/Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 68%] No update step for 'GTest-Debug'
[ 75%] No patch step for 'GTest-Debug'
[ 81%] Performing configure step for 'GTest-Debug'
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/cache.cmake
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/args.cmake
-- [polly] Used toolchain: clang / c++14 support
-- The C compiler identification is AppleClang 17.0.0.17000013
-- The CXX compiler identification is AppleClang 17.0.0.17000013
-- Check for working C compiler: /usr/bin/clang - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/clang++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (0.9s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Build/GTest-Debug-prefix/src/GTest-Debug-build
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
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/libgmockd.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/libgmock_maind.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestTargets-debug.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-assertion-result.h
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Up-to-date: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/libgtestd.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/libgtest_maind.a
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest/args.cmake
[100%] Completed 'GTest-Debug'
[100%] Built target GTest-Debug
-- [hunter] Build step successful (dir: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Build/GTest)
-- [hunter] Cache saved: /Users/sam/projects/hunter/_Base/Cache/raw/bc3a7d254d3ba359f0315b5b96f35a55dc40d5c9.tar.bz2
-- Found GTest: /Users/sam/projects/hunter/_Base/xxxxxxx/858098f/0b4a22b/Install/lib/cmake/GTest/GTestConfig.cmake (found version "1.15.2")
-- Configuring done (28.6s)
-- Generating done (0.5s)
-- Build files have been written to: /Users/sam/samchik7/workspace/projects/lab07/_builds/clang-cxx14
Execute command: [
  `cmake`
  `--build`
  `/Users/sam/samchik7/workspace/projects/lab07/_builds/clang-cxx14`
  `--`
]

[/Users/sam/samchik7/workspace/projects/lab07]> "cmake" "--build" "/Users/sam/samchik7/workspace/projects/lab07/_builds/clang-cxx14" "--"

[ 25%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[ 50%] Linking CXX static library libprint.a
[ 50%] Built target print
[ 75%] Building CXX object CMakeFiles/demo.dir/demo/main.cpp.o
[100%] Linking CXX executable demo
[100%] Built target demo
-
Log saved: /Users/sam/samchik7/workspace/projects/lab07/_logs/polly/clang-cxx14/log.txt
-
Generate: 0:00:30.106915s
Build: 0:00:02.779175s
-
Total: 0:00:32.888259s
-
SUCCESS
sam@Noutbuk-Samvel lab07 % git push origin main
Username for 'https://github.com': samchik7
Password for 'https://samchik7@github.com': 
sam@Noutbuk-Samvel lab07 % git push origin main
Username for 'https://github.com': samchik7
Password for 'https://samchik7@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/samchik7/lab07/'
sam@Noutbuk-Samvel lab07 % 
