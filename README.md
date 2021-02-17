# hasp-lvgl

This is one of my latest projects. I wanted a way to control all of my HA devices without needing to go to the web interface. I stumbled on HASP (HomeAssistantSwitchPanel). This is the main project that most of the people use. In my case, i use the hasp-lvgl. This is a fork of the original HASP project but is standing fully on it's own. It does has some nice extra features in it. The biggest reason i went for LVGL is the abbility to use much cheaper displays. Also you have more options to decide what kind of screen you want to use.


## Screens

![alt text](https://github.com/amauryverschooren/HASP-LVGL/blob/master/screenshot/Screenshot_5.png?raw=true)
![alt text](https://github.com/amauryverschooren/HASP-LVGL/blob/master/screenshot/Screenshot_6.png?raw=true)

On page 1 i can control the led lighting in my room and i can see the temperature and humidity. 

![alt text](https://github.com/amauryverschooren/HASP-LVGL/blob/master/screenshot/Screenshot_1.png?raw=true)
![alt text](https://github.com/amauryverschooren/HASP-LVGL/blob/master/screenshot/Screenshot_7.png?raw=true)

On page 2 i can control the main lights in my room.

![alt text](https://github.com/amauryverschooren/HASP-LVGL/blob/master/screenshot/Screenshot_2.png?raw=true)
![alt text](https://github.com/amauryverschooren/HASP-LVGL/blob/master/screenshot/Screenshot_8.png?raw=true)

On page 3 i can see the weather statistics of my living room.

![alt text](https://github.com/amauryverschooren/HASP-LVGL/blob/master/screenshot/Screenshot_3.png?raw=true)
![alt text](https://github.com/amauryverschooren/HASP-LVGL/blob/master/screenshot/Screenshot_9.png?raw=true)

Page 4 is to enable or disable the darkmode theme.

![alt text](https://github.com/amauryverschooren/HASP-LVGL/blob/master/screenshot/Screenshot_4.png?raw=true)
![alt text](https://github.com/amauryverschooren/HASP-LVGL/blob/master/screenshot/Screenshot_10.png?raw=true)


You also have a Page 0, this page you need to have for navigation buttons.

## Hardware

For the hardware i'm using an [ESP32 TTGO T7](https://nl.aliexpress.com/item/32845357819.html?spm=a2g0o.productlist.0.0.4cb813dbtNkbIe&algo_pvid=b002407d-b062-42e3-a42e-eba6e1a97cfd&algo_expid=b002407d-b062-42e3-a42e-eba6e1a97cfd-13&btsid=0b0a050b16135953084436741e9ee1&ws_ab_test=searchweb0_0,searchweb201602_,searchweb201603_) board to drive a [TFT Screen](https://nl.aliexpress.com/item/32919729730.html?spm=a2g0s.9042311.0.0.75684c4dda4L5t). First i used a Wemos D1 mini but that didn't worked that smooth. When pressing a button, the color change was rather slow. When switched to the ESP32 it was smootyh as butter. Because i'm made a desk version, i wanted to have a battery in it so i could place it everywhere in the house to control my lights etc. It's a regular 18650 LI-ion battery with a simple charger board attached to it. The case i designed myself and is available on [Thingiverse](https://www.thingiverse.com/thing:4766194).

## Software

For the software part you have 2 things you need to have. First you need to have a MQTT server where the esp can talk to. Second you need a config file (.JSONL) to code what needs to be on the screen/pages. All the automations you can do with the yaml automations from HomeAssistant or you can use NodeRed like i did.

![NodeRed Config](https://github.com/amauryverschooren/HASP-LVGL/blob/master/screenshot/nodered.png?raw=true)

I do warn you, the NodeRed flow is very big in a short period of time ;-). I can tell you how everything works but there is a guide that explains it much better then me.


Feel free to use my case and/or [config file](https://github.com/amauryverschooren/HASP-LVGL/blob/master/pages.jsonl) for your build. 

Oh and don't forget to show it also, i'm very curious how you would do it.
