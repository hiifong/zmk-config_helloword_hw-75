# Copyright (c) 2022-2023 XiNGRZ
# SPDX-License-Identifier: MIT

if(CONFIG_HW75_PROTO)

zephyr_library_named(hw75_proto)

include(${ZEPHYR_BASE}/modules/nanopb/nanopb.cmake)

if(CONFIG_HW75_PROTO_USB_COMM)
  zephyr_nanopb_sources(hw75_proto usb_comm.proto)
endif()

if(CONFIG_HW75_PROTO_UART_COMM)
  zephyr_nanopb_sources(hw75_proto uart_comm.proto)
endif()

endif() # CONFIG_HW75_PROTO
