.. module:: Click_8x8

*********
Click 8x8
*********

Used with seven segment displays and 8x8 matrix of LEDs.

    
.. class: LedDisplay(cs, max_devices=1, spidrv=SPI0)

    Constructor takes a chip select pin *cs*, maximum number of devices attached
    *max_devices* and which spi bus *spidrv* the unit is connected to.

    At the moment only 1 device is supported.

    
.. method:: get_device_count()

            Returns the number of devices attached.
        
.. method:: shutdown(dev_num, powerdown)

        *dev_num* is the device id, with 1 device on the bus, the id of the unit is 0.
        *powerdown* is a boolean that is ``True`` or ``False``
        
.. method:: set_scan_limit(dev_num, limit)

        Method that is used for seven segment displays that limits the number of digits.

        *dev_num* is the device id, with 1 device on the bus, the id of the unit is 0.
        *limit* is the number of banks values 0 to 7.
        
.. method:: set_intensity(dev_num, intensity)

        Sets the intensity of the LEDs output.

        *dev_num* is the device id, with 1 device on the bus, the id of the unit is 0.
        *intensity* is the light output intensity values 0 to 15.
        
.. method:: clear_display(dev_num)

        Clears the display by setting all LEDs to 0.
        
.. method:: set_led(dev_num, row, column, state)

        Allows the control of a single LED. 
        *dev_num* is the device id, with 1 device on the bus, the id of the unit is 0.
        *row* is the row 0 to 7
        *column* is the column 0 to 7
        *state* is ``True`` for ON, and ``False`` for OFF
        
.. method:: set_row(dev_num, row, value)

        Controls an entire row.
        *dev_num* is the device id, with 1 device on the bus, the id of the unit is 0.
        *row* to control, values from 0 to 7
        *value* is ``True`` for ON or ``False`` for OFF.
        
.. method:: set_column(dev_num, col, value)

        Controls and entire column.0
        *dev_num* is the device id, with 1 device on the bus, the id of the unit is 0.
        *col* to control, values from 0 to 7
        *value* is ``True`` for ON or ``False`` for OFF.
        
..method:: set_digit(dev_num, digit, value, dp)

        Used with 7 segment displays to set a digit to display on the 7 segments.

        *dev_num* is the device id, with 1 device on the bus, the id of the unit is 0.
        *digit* is the bank from 0 to 7 to display
        *value* is the number value
        *dp* is the decimal point

        
..method:: set_char(dev_num, digit, value, on_off)

        *dev_num* is the device id, with 1 device on the bus, the id of the unit is 0.
        *digit* bank from 0 to 7
        *value* is the character value.
        *on_off* is ``True`` for ON and ``False`` for OFF
        
