foreach(pname gpio_interrupt rtc sleep task_delay timer)

add_executable(${pname} ${pname}.c)

target_link_libraries(${pname} PRIVATE
  pico_stdlib
  pico_multicore
  pico_async_context_freertos
  FreeRTOS-Kernel-Heap4
  pico_cyw43_arch_none
  #unity
)
pico_enable_stdio_uart(${pname} 0)
pico_enable_stdio_usb(${pname} 1)
add_custom_target(flash_${pname}
    picotool load -f $<TARGET_FILE:${pname}> DEPENDS ${pname})
endforeach()
