# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.13.1)
#message("some message $ENV{ZEPHYR_BASE}" )
find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(uart_special)

target_sources(app PRIVATE
    src/main.c
    src/test_uart_config.c
    src/test_uart_poll.c
    src/test_uart_fifo.c
    src/test_uart_pending.c
    )
