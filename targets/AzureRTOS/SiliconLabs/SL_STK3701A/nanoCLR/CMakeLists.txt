#
# Copyright (c) .NET Foundation and Contributors
# See LICENSE file in the project root for full license information.
#

# append nanoCLR source files
list(APPEND NANOCLR_PROJECT_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/main.c)
list(APPEND NANOCLR_PROJECT_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/nanoHAL.cpp)

if(GECKO_FEATURE_USBD_HID)
    list(APPEND NANOCLR_PROJECT_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/usb_hid_app.c)
endif()

# make var global
set(NANOCLR_PROJECT_SOURCES ${NANOCLR_PROJECT_SOURCES} CACHE INTERNAL "make global")
