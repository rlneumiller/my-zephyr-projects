# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(app)

# Include the out-of-tree board
list(APPEND ZEPHYR_EXTRA_MODULES /home/arrel/gits/my_zephyr-projects/esp32c3_supermini)
target_sources(app PRIVATE src/main.c)