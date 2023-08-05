---
layout: post
title:  RINAsense architecture
date:   2023-08-01 16:40:16
description: innovative architecture to prototype IoT devices in RINA networks
tags: rina
categories: rina-iot
---
One of the my main contributions to achieve the TERMINET objectives was the design and development of a RINA architecture for embedded devices to enable RINA networks in IoT environments. Achieving this goal was not trivial because of IoT heterogeneity and IoT limitations on resources. The inherent IoT heterogeneity introduces a high complication to design and implement RINA modules for embedded systems. IoT has many technological IoT platforms, protocols, and wireless communication technologies, so the RINA modules should be able to adapt to IoT technologies. Also, IoT devices are resource-constrained in terms of CPU, memory, network and energy consumption. So, a deep analysis was required to understand the possible limitations of RINA in resource-constrained devices. 

The RINAsense architecture is proposed to implement RINA in resource-constrained devices. The RINAsense architecture is organized in layers.






<div class="row">
    <div class="col-">
    </div>
    <div class="col-">
        {% include figure.html path="assets/img/RINAsenseArquitectura.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-4">
    </div>
</div>
<div class="caption">
    RINAsense architecture for IoT environments.
</div>

#### Architecture Layers
<ul>
    <li>Data Link Layer: oversees moving data into and out of a wireless link in a network. It comprises wireless technologies used in IoT environments. It provides services to the above DIFs to move data between sensors or through a RINA-based IoT gateway to edge nodes or the cloud.</li>
    <li>RINA Layer: provides all RINA components to implement a system with RINA networking capabilities. This layer provides functionalities for transmitting data, controlling the data transmission, and managing the RINA network.</li>
    <li>Application Layer: delivers applications or services to sense the environment(sensors) and make some response (actuators).</li>
    <li>OS and Abstraction Layer: provides a runtime environment to control the previous layers' functionalities. These tasks share a single processing core using the Free Real Time Operating System (FreeRTOS). This layer relies on FreeRTOS because of its extension portability over several microcontroller platforms. In addition, this layer provides a portability sublayer to allow writing cross-platform software to control devices based on the IoT development framework for ESP-IDF, Arduino, or Linux.</li>
</ul>



A instance of the RINAsense architecture is available as open source in i2CAT [Github Reposiroty](https://github.com/Fundacio-i2CAT/rinasense)