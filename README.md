echo $GITHUB_USERNAME
samchik7
sam@Noutbuk-Samvel ~ % cd ${GITHUB_USERNAME}/workspace
sam@Noutbuk-Samvel workspace % pushd .
~/samchik7/workspace ~/samchik7/workspace ~/samchik7/workspace
sam@Noutbuk-Samvel workspace % source scripts/activate
sam@Noutbuk-Samvel workspace % git clone https://github.com/${GITHUB_USERNAME}/lab07 lab08
Cloning into 'lab08'...
remote: Enumerating objects: 100, done.
remote: Counting objects: 100% (100/100), done.
remote: Compressing objects: 100% (81/81), done.
remote: Total 100 (delta 8), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (100/100), 293.21 KiB | 1.84 MiB/s, done.
Resolving deltas: 100% (8/8), done.
sam@Noutbuk-Samvel workspace % cd lab08
sam@Noutbuk-Samvel lab08 % git submodule update --init
sam@Noutbuk-Samvel lab08 % git remote remove origin
sam@Noutbuk-Samvel lab08 % git remote add origin https://github.com/${GITHUB_USERNAME}/lab08
sam@Noutbuk-Samvel lab08 % cat > Dockerfile <<EOF
FROM ubuntu:18.04
EOF
sam@Noutbuk-Samvel lab08 % cat >> Dockerfile <<EOF

RUN apt update
RUN apt install -yy gcc g++ cmake
EOF

sam@Noutbuk-Samvel lab08 % cat >> Dockerfile <<EOF

COPY . print/
WORKDIR print
EOF
sam@Noutbuk-Samvel lab08 % cat >> Dockerfile <<EOF

RUN cmake -H. -B_build -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=_install 
RUN cmake --build _build
RUN cmake --build _build --target install
EOF
sam@Noutbuk-Samvel lab08 % cat >> Dockerfile <<EOF

ENV LOG_PATH /home/logs/log.txt
EOF
sam@Noutbuk-Samvel lab08 % cat >> Dockerfile <<EOF

VOLUME /home/logs
EOF

sam@Noutbuk-Samvel lab08 % 
sam@Noutbuk-Samvel lab08 % cat >> Dockerfile <<EOF

WORKDIR _install/bin
EOF
sam@Noutbuk-Samvel lab08 % cat >> Dockerfile <<EOF

ENTRYPOINT ./demo
EOF
sam@Noutbuk-Samvel lab08 % docker build -t logger .
zsh: command not found: docker
sam@Noutbuk-Samvel lab08 % docker build -t logger .
[+] Building 61.3s (11/14)                                  docker:desktop-linux
 => [internal] load build definition from Dockerfile                        0.0s
 => => transferring dockerfile: 379B                                        0.0s
 => [internal] load metadata for docker.io/library/ubuntu:18.04             4.3s
 => [auth] library/ubuntu:pull token for registry-1.docker.io               0.0s
 => [internal] load .dockerignore                                           0.0s
 => => transferring context: 2B                                             0.0s
 => [1/9] FROM docker.io/library/ubuntu:18.04@sha256:152dc042452c496007f07  2.5s
 => => resolve docker.io/library/ubuntu:18.04@sha256:152dc042452c496007f07  0.0s
 => => sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b 22.71MB / 22.71MB  2.2s
 => => extracting sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3  0.3s
 => [internal] load build context                                           0.0s
 => => transferring context: 1.90MB                                         0.0s
 => [2/9] RUN apt update                                                    4.4s
 => [3/9] RUN apt install -yy gcc g++ cmake                                35.3s 
 => [4/9] COPY . print/                                                     0.0s 
 => [5/9] WORKDIR print                                                     0.0s 
 => ERROR [6/9] RUN cmake -H. -B_build -DCMAKE_BUILD_TYPE=Release -DCMAKE  14.7s 
------                                                                           
 > [6/9] RUN cmake -H. -B_build -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=_install:                                                                       
0.123 -- [hunter] Initializing Hunter workspace (23f1b5a0acffae50fda423388c843a8e7b6e1eb0)                                                                        
0.123 -- [hunter]   https://github.com/cpp-pm/hunter/archive/v0.23.308.tar.gz    
0.123 -- [hunter]   -> /root/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a
2.564 -- The C compiler identification is GNU 7.5.0
2.590 -- The CXX compiler identification is GNU 7.5.0
2.592 -- Check for working C compiler: /usr/bin/cc
2.619 -- Check for working C compiler: /usr/bin/cc -- works
2.620 -- Detecting C compiler ABI info
2.648 -- Detecting C compiler ABI info - done
2.650 -- Detecting C compile features
2.734 -- Detecting C compile features - done
2.735 -- Check for working CXX compiler: /usr/bin/c++
2.769 -- Check for working CXX compiler: /usr/bin/c++ -- works
2.769 -- Detecting CXX compiler ABI info
2.803 -- Detecting CXX compiler ABI info - done
2.807 -- Detecting CXX compile features
2.931 -- Detecting CXX compile features - done
2.932 -- [hunter] Calculating Toolchain-SHA1
3.428 -- [hunter] Calculating Config-SHA1
3.485 -- [hunter] HUNTER_ROOT: /root/.hunter
3.485 -- [hunter] [ Hunter-ID: 23f1b5a | Toolchain-ID: c54aae6 | Config-ID: bf2be25 ]
3.527 -- [hunter] GTEST_ROOT: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Install (ver.: 1.11.0)
4.282 -- [hunter] Building GTest
4.297 loading initial cache file /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/cache.cmake
4.297 loading initial cache file /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/args.cmake
4.337 -- The C compiler identification is GNU 7.5.0
4.366 -- The CXX compiler identification is GNU 7.5.0
4.368 -- Check for working C compiler: /usr/bin/cc
4.396 -- Check for working C compiler: /usr/bin/cc -- works
4.396 -- Detecting C compile features
4.477 -- Detecting C compile features - done
4.478 -- Check for working CXX compiler: /usr/bin/c++
4.507 -- Check for working CXX compiler: /usr/bin/c++ -- works
4.507 -- Detecting CXX compile features
4.635 -- Detecting CXX compile features - done
4.662 -- Configuring done
4.664 -- Generating done
4.665 -- Build files have been written to: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Build
4.685 Scanning dependencies of target GTest-Release
4.690 [  6%] Creating directories for 'GTest-Release'
4.720 [ 12%] Performing download step (download, verify and extract) for 'GTest-Release'
4.725 -- Downloading...
4.725    dst='/root/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
4.725    timeout='none'
4.725 -- Using src='https://github.com/google/googletest/archive/release-1.11.0.tar.gz'
5.427 -- [download 0% complete]
5.427 -- [download 1% complete]
5.492 -- [download 2% complete]
5.494 -- [download 3% complete]
5.494 -- [download 4% complete]
5.494 -- [download 5% complete]
5.548 -- [download 6% complete]
5.548 -- [download 7% complete]
5.549 -- [download 8% complete]
5.549 -- [download 9% complete]
5.549 -- [download 10% complete]
5.549 -- [download 11% complete]
5.603 -- [download 12% complete]
5.603 -- [download 13% complete]
5.603 -- [download 14% complete]
5.603 -- [download 15% complete]
5.603 -- [download 16% complete]
5.604 -- [download 17% complete]
5.605 -- [download 18% complete]
5.605 -- [download 19% complete]
5.605 -- [download 20% complete]
5.605 -- [download 21% complete]
5.605 -- [download 22% complete]
5.605 -- [download 23% complete]
5.606 -- [download 24% complete]
5.732 -- [download 25% complete]
5.733 -- [download 26% complete]
5.733 -- [download 27% complete]
5.846 -- [download 28% complete]
5.847 -- [download 29% complete]
5.847 -- [download 30% complete]
5.847 -- [download 31% complete]
5.847 -- [download 32% complete]
5.854 -- [download 33% complete]
5.854 -- [download 34% complete]
5.921 -- [download 35% complete]
5.921 -- [download 36% complete]
5.921 -- [download 37% complete]
5.921 -- [download 38% complete]
5.921 -- [download 39% complete]
5.921 -- [download 40% complete]
5.923 -- [download 41% complete]
5.980 -- [download 42% complete]
5.980 -- [download 43% complete]
5.981 -- [download 44% complete]
5.981 -- [download 45% complete]
5.981 -- [download 46% complete]
5.981 -- [download 47% complete]
5.981 -- [download 48% complete]
6.036 -- [download 49% complete]
6.036 -- [download 50% complete]
6.036 -- [download 51% complete]
6.036 -- [download 52% complete]
6.037 -- [download 53% complete]
6.037 -- [download 54% complete]
6.037 -- [download 55% complete]
6.037 -- [download 56% complete]
6.038 -- [download 57% complete]
6.038 -- [download 58% complete]
6.038 -- [download 59% complete]
6.039 -- [download 60% complete]
6.039 -- [download 61% complete]
6.039 -- [download 62% complete]
6.093 -- [download 63% complete]
6.093 -- [download 64% complete]
6.093 -- [download 65% complete]
6.093 -- [download 66% complete]
6.093 -- [download 67% complete]
6.094 -- [download 68% complete]
6.094 -- [download 69% complete]
6.094 -- [download 70% complete]
6.095 -- [download 71% complete]
6.095 -- [download 72% complete]
6.095 -- [download 73% complete]
6.095 -- [download 74% complete]
6.095 -- [download 75% complete]
6.095 -- [download 76% complete]
6.095 -- [download 77% complete]
6.095 -- [download 78% complete]
6.096 -- [download 79% complete]
6.096 -- [download 80% complete]
6.096 -- [download 81% complete]
6.097 -- [download 82% complete]
6.147 -- [download 83% complete]
6.147 -- [download 84% complete]
6.147 -- [download 85% complete]
6.147 -- [download 86% complete]
6.148 -- [download 87% complete]
6.148 -- [download 88% complete]
6.148 -- [download 89% complete]
6.148 -- [download 90% complete]
6.148 -- [download 91% complete]
6.148 -- [download 92% complete]
6.148 -- [download 93% complete]
6.150 -- [download 94% complete]
6.150 -- [download 95% complete]
6.150 -- [download 96% complete]
6.150 -- [download 97% complete]
6.150 -- [download 98% complete]
6.150 -- [download 99% complete]
6.150 -- [download 100% complete]
6.153 -- verifying file...
6.153        file='/root/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
6.154 -- Downloading... done
6.176 -- extracting...
6.176      src='/root/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
6.176      dst='/root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Source'
6.176 -- extracting... [tar xfz]
6.202 -- extracting... [analysis]
6.202 -- extracting... [rename]
6.202 -- extracting... [clean up]
6.202 -- extracting... done
6.214 [ 18%] No patch step for 'GTest-Release'
6.227 [ 25%] No update step for 'GTest-Release'
6.238 [ 31%] Performing configure step for 'GTest-Release'
6.243 loading initial cache file /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/cache.cmake
6.243 loading initial cache file /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/args.cmake
6.265 -- The C compiler identification is GNU 7.5.0
6.289 -- The CXX compiler identification is GNU 7.5.0
6.291 -- Check for working C compiler: /usr/bin/cc
6.319 -- Check for working C compiler: /usr/bin/cc -- works
6.319 -- Detecting C compile features
6.402 -- Detecting C compile features - done
6.404 -- Check for working CXX compiler: /usr/bin/c++
6.434 -- Check for working CXX compiler: /usr/bin/c++ -- works
6.435 -- Detecting CXX compile features
6.563 -- Detecting CXX compile features - done
6.567 -- Could NOT find PythonInterp (missing: PYTHON_EXECUTABLE) 
6.567 -- Looking for pthread.h
6.592 -- Looking for pthread.h - found
6.592 -- Looking for pthread_create
6.617 -- Looking for pthread_create - not found
6.618 -- Looking for pthread_create in pthreads
6.639 -- Looking for pthread_create in pthreads - not found
6.639 -- Looking for pthread_create in pthread
6.663 -- Looking for pthread_create in pthread - found
6.663 -- Found Threads: TRUE  
6.667 -- Configuring done
6.670 -- Generating done
6.671 -- Build files have been written to: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Build/GTest-Release-prefix/src/GTest-Release-build
6.678 [ 37%] Performing build step for 'GTest-Release'
6.695 Scanning dependencies of target gtest
6.699 [ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
9.723 [ 25%] Linking CXX static library ../lib/libgtest.a
9.741 [ 25%] Built target gtest
9.750 Scanning dependencies of target gtest_main
9.752 Scanning dependencies of target gmock
9.755 [ 37%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
9.757 [ 50%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
10.06 [ 62%] Linking CXX static library ../lib/libgtest_main.a
10.07 [ 62%] Built target gtest_main
10.83 [ 75%] Linking CXX static library ../lib/libgmock.a
10.84 [ 75%] Built target gmock
10.85 Scanning dependencies of target gmock_main
10.85 [ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
11.12 [100%] Linking CXX static library ../lib/libgmock_main.a
11.13 [100%] Built target gmock_main
11.14 [ 43%] Performing install step for 'GTest-Release'
11.16 [ 25%] Built target gtest
11.17 [ 50%] Built target gmock
11.18 [ 75%] Built target gmock_main
11.19 [100%] Built target gtest_main
11.20 Install the project...
11.20 -- Install configuration: "Release"
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-spec-builders.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-function-mocker.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/gmock-pp.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/custom
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/custom/README.md
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/gmock-port.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-more-matchers.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-more-actions.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-nice-strict.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-matchers.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-actions.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-cardinalities.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/libgmock.a
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/libgmock_main.a
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/pkgconfig/gmock.pc
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/cmake/GTest/GTestTargets-release.cmake
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
11.20 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-death-test.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-printers.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-typed-test.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-param-test.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-matchers.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-port.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-internal.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/custom
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/custom/gtest.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/custom/README.md
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-string.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-test-part.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest_pred_impl.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-spi.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-message.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest_prod.h
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/libgtest.a
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/libgtest_main.a
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/pkgconfig/gtest.pc
11.20 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
11.21 loading initial cache file /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/args.cmake
11.22 [ 50%] Completed 'GTest-Release'
11.23 [ 50%] Built target GTest-Release
11.23 Scanning dependencies of target GTest-Debug
11.24 [ 56%] Creating directories for 'GTest-Debug'
11.26 [ 62%] Performing download step (download, verify and extract) for 'GTest-Debug'
11.26 -- verifying file...
11.26        file='/root/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
11.27 -- File already exists and hash match (skip download):
11.27   file='/root/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
11.27   SHA1='7b100bb68db8df1060e178c495f3cbe941c9b058'
11.27 -- extracting...
11.27      src='/root/.hunter/_Base/Download/GTest/1.11.0/7b100bb/release-1.11.0.tar.gz'
11.27      dst='/root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Source'
11.27 -- extracting... [tar xfz]
11.29 -- extracting... [analysis]
11.29 -- extracting... [rename]
11.29 -- extracting... [clean up]
11.29 -- extracting... done
11.30 [ 68%] No patch step for 'GTest-Debug'
11.31 [ 75%] No update step for 'GTest-Debug'
11.32 [ 81%] Performing configure step for 'GTest-Debug'
11.32 loading initial cache file /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/cache.cmake
11.32 loading initial cache file /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/args.cmake
11.34 -- The C compiler identification is GNU 7.5.0
11.37 -- The CXX compiler identification is GNU 7.5.0
11.37 -- Check for working C compiler: /usr/bin/cc
11.39 -- Check for working C compiler: /usr/bin/cc -- works
11.40 -- Detecting C compile features
11.47 -- Detecting C compile features - done
11.47 -- Check for working CXX compiler: /usr/bin/c++
11.50 -- Check for working CXX compiler: /usr/bin/c++ -- works
11.50 -- Detecting CXX compile features
11.63 -- Detecting CXX compile features - done
11.63 -- Could NOT find PythonInterp (missing: PYTHON_EXECUTABLE) 
11.63 -- Looking for pthread.h
11.66 -- Looking for pthread.h - found
11.66 -- Looking for pthread_create
11.68 -- Looking for pthread_create - not found
11.69 -- Looking for pthread_create in pthreads
11.71 -- Looking for pthread_create in pthreads - not found
11.71 -- Looking for pthread_create in pthread
11.73 -- Looking for pthread_create in pthread - found
11.73 -- Found Threads: TRUE  
11.74 -- Configuring done
11.74 -- Generating done
11.74 -- Build files have been written to: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Build/GTest-Debug-prefix/src/GTest-Debug-build
11.75 [ 87%] Performing build step for 'GTest-Debug'
11.77 Scanning dependencies of target gtest
11.77 [ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
12.93 [ 25%] Linking CXX static library ../lib/libgtestd.a
12.95 [ 25%] Built target gtest
12.96 Scanning dependencies of target gtest_main
12.96 Scanning dependencies of target gmock
12.97 [ 37%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
12.97 [ 50%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
13.21 [ 62%] Linking CXX static library ../lib/libgtest_maind.a
13.22 [ 62%] Built target gtest_main
13.55 [ 75%] Linking CXX static library ../lib/libgmockd.a
13.57 [ 75%] Built target gmock
13.58 Scanning dependencies of target gmock_main
13.58 [ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
13.87 [100%] Linking CXX static library ../lib/libgmock_maind.a
13.88 [100%] Built target gmock_main
13.89 [ 93%] Performing install step for 'GTest-Debug'
13.91 [ 25%] Built target gtest
13.92 [ 50%] Built target gmock
13.93 [ 75%] Built target gmock_main
13.93 [100%] Built target gtest_main
13.94 Install the project...
13.94 -- Install configuration: "Debug"
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-spec-builders.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-function-mocker.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/gmock-pp.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/custom
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/custom/README.md
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/internal/gmock-port.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-more-matchers.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-more-actions.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-nice-strict.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-matchers.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-actions.h
13.94 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gmock/gmock-cardinalities.h
13.94 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/libgmockd.a
13.95 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/libgmock_maind.a
13.95 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/pkgconfig/gmock.pc
13.95 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
13.95 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
13.95 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/cmake/GTest/GTestTargets-debug.cmake
13.95 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
13.95 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-death-test.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-printers.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-typed-test.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-param-test.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-matchers.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-port.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-internal.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/custom
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/custom/gtest.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/custom/README.md
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/internal/gtest-string.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-test-part.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest_pred_impl.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-spi.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest-message.h
13.95 -- Up-to-date: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/include/gtest/gtest_prod.h
13.95 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/libgtestd.a
13.95 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/libgtest_maind.a
13.95 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/pkgconfig/gtest.pc
13.95 -- Installing: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
13.95 loading initial cache file /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest/args.cmake
13.96 [100%] Completed 'GTest-Debug'
13.97 [100%] Built target GTest-Debug
13.98 -- [hunter] Build step successful (dir: /root/.hunter/_Base/23f1b5a/c54aae6/bf2be25/Build/GTest)
14.48 -- [hunter] Cache saved: /root/.hunter/_Base/Cache/raw/0d84d97bced5fc5eb928fa8bd50e4381beb4ee02.tar.bz2
14.62 
14.62 [hunter ** INTERNAL **] Link script failed: 1, , CMake Error at /root/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/scripts/link-all.cmake:1 (cmake_minimum_required):
14.62   CMake 3.12 or higher is required.  You are running version 3.10.2
14.62 
14.62 
14.62 
14.62 [hunter ** INTERNAL **] [Directory:/root/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest]
14.62 
14.62 ------------------------------ ERROR -----------------------------
14.62     https://hunter.readthedocs.io/en/latest/reference/errors/error.internal.html
14.62 ------------------------------------------------------------------
14.62 
14.62 CMake Error at /root/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_error_page.cmake:12 (message):
14.62 Call Stack (most recent call first):
14.62   /root/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_internal_error.cmake:13 (hunter_error_page)
14.62   /root/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_unpack_directory.cmake:153 (hunter_internal_error)
14.62   /root/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:103 (hunter_unpack_directory)
14.62   /root/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:635 (hunter_save_to_cache)
14.62   /root/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:302 (hunter_download)
14.62   /root/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
14.62   CMakeLists.txt:24 (hunter_add_package)
14.62 
14.62 
14.62 -- Configuring incomplete, errors occurred!
14.62 See also "/print/_build/CMakeFiles/CMakeOutput.log".
------

 3 warnings found (use docker --debug to expand):
 - WorkdirRelativePath: Relative workdir "print" can have unexpected results if the base image changes (line 7)
 - LegacyKeyValueFormat: "ENV key=value" should be used instead of legacy "ENV key value" format (line 13)
 - JSONArgsRecommended: JSON arguments recommended for ENTRYPOINT to prevent unintended behavior related to OS signals (line 19)
Dockerfile:9
--------------------
   7 |     WORKDIR print
   8 |     
   9 | >>> RUN cmake -H. -B_build -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=_install
  10 |     RUN cmake --build _build
  11 |     RUN cmake --build _build --target install
--------------------
ERROR: failed to solve: process "/bin/sh -c cmake -H. -B_build -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=_install" did not complete successfully: exit code: 1
sam@Noutbuk-Samvel lab08 % docker images
REPOSITORY   TAG       IMAGE ID   CREATED   SIZE
sam@Noutbuk-Samvel lab08 % mkdir logs
sam@Noutbuk-Samvel lab08 % docker run -it -v "$(pwd)/logs/:/home/logs/" logger
Unable to find image 'logger:latest' locally
docker: Error response from daemon: pull access denied for logger, repository does not exist or may require 'docker login'

Run 'docker run --help' for more information
sam@Noutbuk-Samvel lab08 % 
sam@Noutbuk-Samvel lab08 % text1
zsh: command not found: text1
sam@Noutbuk-Samvel lab08 % text2
zsh: command not found: text2
sam@Noutbuk-Samvel lab08 % ext3
zsh: command not found: ext3
sam@Noutbuk-Samvel lab08 % docker run -it -v "$(pwd)/logs/:/home/logs/" logger
text1
text2
text3
<C-D>
zsh: parse error near `\n'
sam@Noutbuk-Samvel lab08 % docker inspect logger
[]
Error: No such object: logger
sam@Noutbuk-Samvel lab08 % cat logs/log.txt
cat: logs/log.txt: No such file or directory
sam@Noutbuk-Samvel lab08 % gsed -i 's/lab07/lab08/g' README.md
sed: 1: "README.md": invalid command code R
sam@Noutbuk-Samvel lab08 % vim .travis.yml

zsh: suspended  vim .travis.yml
sam@Noutbuk-Samvel lab08 % git add Dockerfile
sam@Noutbuk-Samvel lab08 % git add .travis.yml
fatal: pathspec '.travis.yml' did not match any files
sam@Noutbuk-Samvel lab08 % git commit -m"adding Dockerfile"
[main c9e1925] adding Dockerfile
 1 file changed, 19 insertions(+)
 create mode 100644 Dockerfile
sam@Noutbuk-Samvel lab08 %  git push origin main
