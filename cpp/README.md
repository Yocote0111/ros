# Commands
<https://cmake.org/cmake/help/v3.11/command/include_directories.html>
```
cmake_minimum_required(VERSION ${VERSION})

project(${PROJECT_NAME})

message(${MESSAGE_CONTENT})

set(${ARG} ${VALUE})


include_directories(${INCLUDE_DIR}) # ヘッダファイルファイルのインクルードパス
link_libraries(${LIB_NAME}) # 非推奨
add_library(${LIB_NAME} [STATIC|SHARED] ${SOURCE}) # Windows [.lib|.dll], Linux [.a|.so]
add_executable(${EXE_NAME} {SOURCE}) # Windows [.exe], Linux []
target_compile_options(${EXE_NAME} [PRIVATE] ${OPTS}) 
target_link_libraries(${EXE_NAME} ${LIB_NAME})
target_include_diractries(${EXE_NAME} [PRIVATE] ${INCLUDE_DIR}) # ヘッダファイルのインクルードパス
```

## Control Scripts
```
if(condition0)
  ...
elseif(condition1)
  ...
else(condition0)
  ...
endif(condition0)
```

```
foreach(VAR [ARGS])
  ...
  command(${VAR})
  ...
endforeach(VAR)
```

```
function(${FUNCTION_NAME})
  ...
endfinction()
```

```
macro(${MACRO_NAME})
  ...
endmacro()
```

```
set(CMAKE_VERBOSE_MAKEFILE TRUE) # 出力情報を増やす
set(EXECUTABLE_OUTPUT_PATH build) # 出力先を指定
```

# Environmental Variables
<https://cmake.org/cmake/help/v3.11/manual/cmake-env-variables.7.html>
<https://cmake.org/cmake/help/v3.11/manual/cmake-variables.7.html>
```
get_cmake_property(_variableNames VARIABLES)
list (SORT _variableNames)
foreach (_variableName ${_variableNames})
    message(STATUS "${_variableName}=${${_variableName}}")
    endforeach()

```
