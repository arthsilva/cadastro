#arquivo para gerar o make file
cmake_minimum_required(VERSION 3.7.0)

project(Cadastro)

set(PROJECT_VERSION_MAJOR 0)
set(PROJECT_VERSION_MINOR 1)
set(PROJECT_VERSION_PATCH 0) #ainda não tenho nenhuma correção

set(CMAKE_C_FLAGS "-D_GNU_SOURCE -Wall -std=c99") #
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin) #diretório para onde vai os binários gerados
set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR}/lib) #define o diretório das bibliotecas
set(CMAKE_BUILD_TYPE Debug) #definir qual vai ser o profile de compilação

#Criar o binário
add_executable(cadastro "")
#adicionar os arquivos aqui
target_sources(cadastro
    PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/src/main.c
)
#adicionar os arquivos de inclusão
target_include_directories(cadastro
    PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/include
)