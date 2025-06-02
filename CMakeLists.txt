cmake_minimum_required(VERSION 4.0.2)
project(BattleCity)

# Подключение GLFW (выберите ОДИН способ)
# Способ 1: Через find_package (если GLFW установлен)
find_package(OpenGL REQUIRED)
add_subdirectory(external/glfw)
# Способ 2: Через FetchContent (автоматическая загрузка)
# include(FetchContent)
# FetchContent_Declare(glfw GIT_REPOSITORY https://github.com/glfw/glfw.git GIT_TAG 3.3.8)
# FetchContent_MakeAvailable(glfw)

# Создание исполняемого файла
add_executable(BattleCity src/main.cpp)

# Линковка библиотек
target_link_libraries(BattleCity glfw)

