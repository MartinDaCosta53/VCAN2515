cmake_minimum_required(VERSION 4.2)
project(VCAN2515)

set(CMAKE_CXX_STANDARD 11)

include_directories(Arduino)
include_directories(src)

add_library(VCAN2515 OBJECT
        src/CAN2515.cpp
        src/CAN2515.h

        Arduino/Arduino.h
        Arduino/Streaming.h
        Arduino/SPI.h
        Arduino/Wire.h
        Arduino/EEPROM.h
        Arduino/ACAN2515.h

        examples/VLCB_1in1out/VLCB_1in1out.ino
        examples/VLCB_4in4out/VLCB_4in4out.ino
        examples/VLCB_4in4out_slot/VLCB_4in4out_slot.ino
        examples/VLCB_empty/VLCB_empty.ino
        examples/VLCB_long_message_example/VLCB_long_message_example.ino
)
