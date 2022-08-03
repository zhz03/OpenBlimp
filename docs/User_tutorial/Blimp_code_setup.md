# Blimp Code Setup

To control your embedded system, you need to upload code to your Arduino Board. However, the Arduino code really depends on your hardware setup. 

In our previous chapter, we talk about different ways of communication. In  Openblimp User tutorials, we only provide manual control Arduino Code, for autonomous control or other algorithms extension, please refer to [Developer Tutorial]()

## Code logic

In the OpenBlimp manual control, the message that communicates between controller(laptop, cellphone app) and blimp control board is just motion commands. For example, our message format is `~00000000`.

Note: 

- The index ~
- The pwm command and direction command

## Different ways of communication

### Bluetooth connection



### P2P connection

To set up P2P connection, you need to have two Control board. One as `Master` board, the other as `Slave` board. Normally, the one that you connect with your laptop should be set as `Master` board, and the one on blimp should be set as `Slave` board. 

Here are the steps to setup P2P connection:

**Step 1: Acquire the MAC address** 

Before uploading corresponding code to the `Master` and `Slave` board, you need to know the MAC address of the master and slave board.

For ESP8266 chip:

For ESP32 chip:

**Step 2: Upload code to the master board** 



**Step 3: Upload code to the slave board**



### WebSocket connection

For the WebSocket connection, you only need to upload the code once to your control board on the blimp. But it requires other setup. 

**Step 1: Setup an AP (Access Point)**

You need to set up a router or an access point before you proceed WebSocket communication. After your access point setup, you need to write down its `Wi-Fi name` and `password` for later use. 

**Note:** 

For the control board we provided, your router or access point should have 2.4G Wi-Fi instead of 5G Wi-Fi because our provided control board won't work on 5G Wi-Fi. 

**Step 2: Upload code to the blimp control board**

You need upload our WebSocket code accordingly with some small modification based on your Chip and Access point. 

Use the [Code]() we provide and modify the following parts: 

```

```

