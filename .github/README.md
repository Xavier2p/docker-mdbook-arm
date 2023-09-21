# `mdbook` Docker Image for ARM

*Forked from [peaceiris/docker-mdbook](https://github.com/peaceiris/docker-mdbook).*

[![GitHub](https://img.shields.io/github/license/Xavier2p/docker-mdbook-arm?style=for-the-badge&logo=github&color=yellow)
](https://github.com/xavier2p/docker-mdbook-arm/blob/main/LICENSE)
[![GitHub release (with filter)](https://img.shields.io/github/v/release/Xavier2p/docker-mdbook-arm?style=for-the-badge&logo=github-actions)
](https://github.com/xavier2p/docker-mdbook-arm/releases/latest)
[![GitHub Release Date - Published_At](https://img.shields.io/github/release-date/Xavier2p/docker-mdbook-arm?style=for-the-badge&logo=docker)
](https://github.com/xavier2p/docker-mdbook-arm/releases)
[![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/Xavier2p/docker-mdbook-arm/cd.yml?style=for-the-badge&logo=github-actions&label=CD)
](https://github.com/xavier2p/docker-mdbook/actions-arm)

## Alpine Base Docker Image for mdBook

Alpine base Docker Image for [rust-lang/mdBook](https://github.com/rust-lang/mdBook).

### Docker Compose

Create your `docker-compose.yml` like the following, or just use the one in this repository.

```yaml
version: '3'

services:
  mdbook:
    container_name: mdbook
    image: ghcr.io/xavier2p/mdbook:latest
    stdin_open: true
    tty: true
    ports:
      - 3000:3000
    volumes:
      - ${PWD}:/book
    command:
      - serve
      - --hostname
      - '0.0.0.0'
```

### Usage

```sh
# Run "mdbook serve"
docker-compose up

# Run a command of mdBook
docker-compose run --rm mdbook init
```

## GitHub Actions for mdBook

The mdBook Setup GitHub Action is recommended.

- [peaceiris/actions-mdbook: GitHub Actions for mdBook (rust-lang/mdBook) ⚡️ Setup mdBook quickly and build your site fast. Linux (Ubuntu), macOS, and Windows are supported.](https://github.com/peaceiris/actions-mdbook)

## License

```txt
MIT License

Copyright (c) 2020 peaceiris (Shohei Ueda)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
