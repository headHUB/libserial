ADD_LIBRARY(libserial_static STATIC
	PosixSignalDispatcher.cpp
    SerialPort.cpp
    SerialStream.cc
    SerialStreamBuf.cc
)

SET_TARGET_PROPERTIES(libserial_static
	PROPERTIES
	PREFIX ""
	SUFFIX .la
)

TARGET_INCLUDE_DIRECTORIES(libserial_static PUBLIC ${CMAKE_CURRENT_LIST_DIR})