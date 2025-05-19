# Zmk Config
This repo holds my ZMK configs for various boards and projects

### Multi Macropad
- multiple 3x3 macropads networked to a main control unit
- support for expansion

# Build Locally
1. follow the zmk local env instructions
2. clone the module repo for zmk-multi-module
3. run the following commands (replace CONFIG_PATH with the dir you cloned this repo into and MODULE_PATH with the multi-module dir)
    `west build -d build/control -p -b nice_nano -- -DSHIELD=multi_control -DZMK_CONFIG="/CONFIG_PATH/zmk-config" -DZMK_EXTRA_MODULES="/MODULE_PATH/zmk-multi-module`
    `west build -d build/peripherals/one -p -b nice_nano -- -DSHIELD=multi_peripheral_one -DZMK_CONFIG="/CONFIG_PATH/zmk-config" -DZMK_EXTRA_MODULES="/MODULE_PATH/zmk-multi-module`
    `west build -d build/peripherals/two -p -b nice_nano -- -DSHIELD=multi_peripheral_two -DZMK_CONFIG="/CONFIG_PATH/zmk-config" -DZMK_EXTRA_MODULES="/MODULE_PATH/zmk-multi-module`