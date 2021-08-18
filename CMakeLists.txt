# CMAKE VERSION
cmake_minimum_required(VERSION 3.18.0)

include(cmake/udph.cmake)

project_create(libudph_Container)

PROJECT_SET_NAMESPACE(libudph_Container libudph)

TARGET_CREATE_LIB(Container INTERFACE)
TARGET_APPEND_HDR(
	Container
	"libudph/Container/Container.h"
	"libudph/Container/Iterator.h"
)

TARGET_LINK(Container)

TARGET_PACKAGE(Container)

FINALIZE()