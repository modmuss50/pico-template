cmake_minimum_required(VERSION 3.16)

include(pico-sdk/pico_sdk_init.cmake)

project(PicoTemplate)

pico_sdk_init()

add_executable(PicoTemplate main.cpp)

# Link with the pico stdlib
target_link_libraries(PicoTemplate pico_stdlib hardware_adc)

# Create map/bin/hex/uf2 files
pico_add_extra_outputs(PicoTemplate)

# Enable USB serial
pico_enable_stdio_usb(PicoTemplate 1)
pico_enable_stdio_uart(PicoTemplate 0)