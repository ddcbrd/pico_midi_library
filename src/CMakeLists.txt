project(midi)

add_library(midi STATIC
    midi_Namespace.h
    midi_Defs.h
    midi_Message.h
    midi_Platform.h
    midi_Settings.h
    MIDI.cpp
    MIDI.hpp
    MIDI.h
    serialMIDI.h
    USB-MIDI_Namespace.h
    USB-MIDI_defs.h
    USB-MIDI.h
)
target_link_libraries(midi PRIVATE
    pico_stdlib
    hardware_uart
    tinyusb_device 
    tinyusb_board )
