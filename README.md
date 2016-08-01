### TODO: Présentation du module

<<<<<<< HEAD
#Installation
>Require :
* node
* npm

##Cloning sources and installation of Node modules
```bash
git clone https://github.com/coast-team/mute-demo
npm install
```

## Setup signaling server
This mute editor provides its own signaling server but you can use an external one by providing the server hostname and port as environment variable (`SIGNALING_SERVER_HOST`, `SIGNALING_SERVER_PORT`)

By default: `ws://localhost:8000` (you may use `ws://sigver-coastteam.rhcloud.com:8000`)

##DB installation

>Require :
* MongoDB 3.0.4

###DB configuration
```
mongo
> use mute
> db.createUser(
  {
    user: "mute",
    pwd: "mute",
    roles: [ { role: "userAdmin", db: "mute" } ]
  }
)
```
##Launch app
>In mute-demo folder

```
node app.js
```
#Architecture

#See also

* [**mute-client**](https://github.com/MatthieuNICOLAS/mute-client)
* [**mute-server**](https://github.com/MatthieuNICOLAS/mute-server)
=======
# Installation

```
npm install mute-server
```

If you want to use the socketIOAdapter provided in this module, you will need to install **socket.io** too:

```
npm install socket.io
```

# Utilisation

**In your app.js file:**

```
var server = require('http').createServer(app),
var Coordinator = require('mute-server').Coordinator,
var SocketIOAdapter = require('mute-server').SocketIOAdapter;

var coordinator = new Coordinator();
var socketIOAdapter = new SocketIOAdapter(server, coordinator);
coordinator.setNetwork(socketIOAdapter);
```

### Network

The network architecture provided consist in an **central server** communicating with clients using WebSockets, using **socket.io**, and broadcasting the modifications made by users to the others.
If you don't want to use **socket.io**, you can easily **implement your own network architecture**, as long as you respect the **name of the events and the data structure** used to communicate between the **coordinator and the network adapter**.

# See also

* [**mute-demo**](https://github.com/MatthieuNICOLAS/mute-demo)
* [**mute-client**](https://github.com/MatthieuNICOLAS/mute-client)
>>>>>>> 3651615baf95505b96c74a08a67d35ed49efe99e
* [**mute-structs**](https://github.com/MatthieuNICOLAS/mute-structs)
* [**mute-utils**](https://github.com/MatthieuNICOLAS/mute-utils)

## License

<<<<<<< HEAD
**mute-demo** is licensed under the GNU General Public License 3.
=======
**mute-server** is licensed under the GNU General Public License 3.
>>>>>>> 3651615baf95505b96c74a08a67d35ed49efe99e

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT
ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program. If not, see <http://www.gnu.org/licenses/>.

The documentation, tutorial and source code are intended as a community
resource and you can basically use, copy and improve them however you want.
<<<<<<< HEAD
Included works are subject to their respective licenses.
=======
Included works are subject to their respective licenses.
>>>>>>> 3651615baf95505b96c74a08a67d35ed49efe99e
