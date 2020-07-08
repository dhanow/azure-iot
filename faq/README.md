Table of contents
1. [Protocol](#protocol)


## Protocol

* Which protocol should be used, if the payload needs to be small? <br>
    
    You should use AMQP. AMQP is a binary protocol, so its payload is more compact than the one in HTTPS. It is also the 
    only protocol that supports field gateways with connection multiplexing across IoT sensors. AMQP also uses port 567, 
    which is allowed on your Azure IoT hub.<br>

    You should not use MQTT or MQTT over SebSockets. MQTT uses port 8883 or port 443 (using MQTT over WebSockets) on the 
    networks that allows HTTPS protocols only.MQTT is a binary protocol like AMQP, so it has a relatively compact payload 
    size. However, it does not support connection multiplexing.

    You should not use HTTPS, HTTPS has the biggest payload size compared to more compact binary protocols like AMQP or 
    MQTT, and it uses port 443. However, it does not support connection multiplexing, which does not meet the technical 
    and security requirements of your organization.
    
    

  
