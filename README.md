# zmk-sofle-dongle

## build

build relative to this repo:
```
# init west
$ west init -l config/
$ west update
$ west zephyr-export

# build targets
$ west build -p -s zmk/app -d ../zmk-builds/test_05/dongle -b nice_nano_v2 -S studio-rpc-usb-uart -- -DZMK_CONFIG=`pwd`/config -DSHIELD="eyelash_sofle_central_dongle dongle_display" -DZMK_EXTRA_MODULES=`pwd`/eyelash-sofle-module -DCONFIG_ZMK_STUDIO=y -DCONFIG_ZMK_STUDIO_LOCKING=n
$ west build -p -s zmk/app -d ../zmk-builds/test_05/left -b nice_nano_v2 -- -DZMK_CONFIG=`pwd`/config -DSHIELD="eyelash_sofle_peripheral_left nice_view" -DZMK_EXTRA_MODULES=`pwd`/eyelash-sofle-module
$ west build -p -s zmk/app -d ../zmk-builds/test_05/right -b nice_nano_v2 -- -DZMK_CONFIG=`pwd`/config -DSHIELD="eyelash_sofle_peripheral_right nice_view" -DZMK_EXTRA_MODULES=`pwd`/eyelash-sofle-module
$ west build -p -s zmk/app -d ../zmk-builds/test_05/settings_reset -b nice_nano_v2 -- -DZMK_CONFIG=`pwd`/config -DSHIELD=settings_reset -DZMK_EXTRA_MODULES=`pwd`/eyelash-sofle-module
```
