# Stop grinder on dose
Eureka Mignon (or any other grinder ) stop on dose 

It doesn't need any modification on the grinder, only needs timer mode. 
My Silenzio is set to maximum duration and once it gets to desired dose it kills the power. 
It can run with any grinder that has timer mode (or you can hold the grind button all the time) and you need to 3D print different case. 

Tuning required is:
  - calibrating the load cell
  - stop before weight (in grams to stop before the desired walue, otherwise it will overshoot). 
There are few physical buttons:
  - power (I don't know how long will the screen last if it's on all the time). 
  - tare 
  - reset switch (to enable the grinder once it's powered off if the weight is exceeded)
  
It's using:
  - ESP8266
  - loadcell 750g
  - relay 
  - OLED Display Module 128X64 I2C SSD1306
  - There are two plugs behind (male and female) where you connect the main power and the grinder. 

Coding is done through ESPHome so it's automatically integrated into Home Assistent. 

Home assistent is currently used only for:  
  - setting the wanted dose
  - setting the offset 
  - display live weight
  - manual tare the scale
  
Inside HA you need to create two helpers that will be used for DOSE and OFFSET values:
  - input_number.coffe_weight
  - input_number.coffe_offset
  
