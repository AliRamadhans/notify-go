# notify-go
Line Notify For Go
# golang line notify

[![PkgGoDev](https://pkg.go.dev/badge/github.com/AliRamadhans/notify-go)](https://pkg.go.dev/github.com/AliRamadhans/notify-go)
[![Build Status](https://travis-ci.org/AliRamadhans/notify-go.svg?branch=master)](https://travis-ci.org/AliRamadhans/notify-go)
[![Go Report Card](https://goreportcard.com/badge/github.com/AliRamadhans/notify-go)](https://goreportcard.com/report/github.com/AliRamadhans/notify-go)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Install

```bash
go get -u github.com/AliRamadhans/notify-go
```

## Usage

```go
package main

import "github.com/AliRamadhans/notify-go"

func main() {
    accessToken := "Here_your_oauth_notify"
    message := "LeeVersion an BotLine  Example For  LineNotify!"

    if err := notify-go.SendText(accessToken, message); err != nil {
        panic(err)
    }
}
```

### Send Notify With Online Image

```go
accessToken := "your-access-token"
message := "your message. must not be empty"
imageURL := "image url. ex) https://..."

if err := notify-go.SendImage(accessToken, message, imageURL); err != nil {
    panic(err)
}
```

### Send Notify With Local Image (only jpg, png)
```go
accessToken := "your-access-token"
message := "your message. must not be empty"
imagePath := "/your/image/path.png"

if err := notify-go.SendLocalImage(accessToken, message, imagePath); err != nil {
    panic(err)
}
```

### Send Notify With Sticker

Sticker List is [See Here](https://devdocs.line.me/files/sticker_list.pdf)

```go
accessToken := "your-access-token"
message := "your message. must not be empty"
stickerPackageId := 1
stickerId := 113

if err := notify-go.SendSticker(accessToken, message, stickerPackageId, stickerId); err != nil {
    panic(err)
}
```
