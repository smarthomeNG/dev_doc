
.. index:: Node.js installieren

.. role:: bluesup
.. role:: redsup

=====================
Node.js :redsup:`new`
=====================

Einige Software Pakete, die zusätzlich installiert werden um z.B.  das Zigbee2Mqtt Gateway oder das MobileAlerts
Gateway zu unterstützen, benötigen node.js. Deshalb wird für diejenigen, die es benötigen, im folgenden die
Installation von Node.js und Node Packet Manager (npm) beschrieben.

.. contents:: Schritte der Installation
   :local:

Node.js Installation
====================

Vor der Installation von Node.js und nvm sollte das Betriebssystem auf den aktuellen Stand gebracht werden.
Dazu sollten die System Repositories auf den aktuellen Stand gebracht werden:

.. code-block:: bash

    sudo apt update


Anschließend sollten die Pakete auf die aktuellste Version gebracht werden:

.. code-block:: bash

    sudo apt upgrade

|

Anschließend können mit dem folgenden Kommando node.js und npm installiert werden:

.. code-block:: bash

    sudo apt install nodejs npm -y

|

Anschließend kann die Installation mit den folgenden Kommandos überprüft werden, die die Versionen von node.js und npm
ausgeben:

.. code-block:: bash

    node -v

und

.. code-block:: bash

    nopm -v

|

Zigbee2MQTT Gateway installieren
================================

...

.. code-block:: bash

    # Install pnpm
    wget -qO- https://get.pnpm.io/install.sh | sh -

    # Create a directory for zigbee2mqtt and set your user as owner of it
    sudo mkdir /opt/zigbee2mqtt
    sudo chown -R ${USER}: /opt/zigbee2mqtt

    # Clone Zigbee2MQTT repository
    git clone --depth 1 https://github.com/Koenkk/zigbee2mqtt.git /opt/zigbee2mqtt

    # Install dependencies (as user "smarthome")
    cd /opt/zigbee2mqtt
    pnpm install --frozen-lockfile

|

MobileAlerts Proxy installieren
===============================

...

.. code-block:: bash

    # Create a directory for mobile alerts proxy and set your user as owner of it
    sudo mkdir /opt/ma
    sudo chown -R ${USER}: /opt/ma

    # Clone mobile alerts proxy repository
    git clone https://github.com/sarnau/MMMMobileAlerts.git /opt/ma

|

MobileAlerts Proxy konfigurieren
--------------------------------

...

https://github.com/sarnau/MMMMobileAlerts/blob/master/maserver/README.md

