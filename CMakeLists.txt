cmake_minimum_required(VERSION 3.20)
project(SFML_Lab LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Поиск SFML компонентов
find_package(SFML COMPONENTS Graphics Window System CONFIG REQUIRED)

# Создание исполняемого файла из main.cpp
add_executable(SFML_Lab main.cpp)

# Подключение библиотек SFML
target_link_libraries(SFML_Lab PRIVATE
    SFML::Graphics
    SFML::Window
    SFML::System
)