cmake_minimum_required(VERSION 2.8.9)
project (TestLibrary)

#For the shared library:
#set ( PROJECT_LINK_LIBS libtestStudent.so )
#link_directories( /home/mrlaw/CmakeProject/sharedlibStudent/build )

#For the static library:
set ( PROJECT_LINK_LIBS libtestStudent.a )
link_directories( /home/mrlaw/CmakeProject/staticlibStudent/build )

include_directories(/home/mrlaw/CmakeProject/sharedlibStudent/include)

add_executable(libtest libtest.cpp)
target_link_libraries(libtest ${PROJECT_LINK_LIBS} )
