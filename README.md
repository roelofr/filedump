# FileDump

Simple WebRTC file transfer, using Express as signal server.

Contents are transfered peer-to-peer, so the server only needs to send minimal
JSON data.  All content-communication is done directly, with no knowledge being
shared to the server.

**Disclaimer**: This is a hobby project, safety and functionality not
guaranteed. Please don't use for nefarious purposes.

## License

This software is licensed under the GNU General Public License version 3, which
is available [here](./LICENSE.md).

```
Filedump - WebRTC-based, minimal-knowledge file transfer
Copyright (C) 2020 Roelof Roos

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
```

## Usage

It's available as Docker image, so simply mount that.

```
docker up -P 8080:8080 docker.pkg.github.com/roelofr/filedump/server:latest
```

## Requirements (non-Docker)

To run this yourself, you'll need NodeJS and Yarn (npm should work too, but I
use Yarn).

```
yarn install
yarn build
yarn start
```

Now an ExpressJS server has started, which serves the static content.
Have fun :smile:.
