# nvidia-video-codec

[![LICENSE](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Redistributable headers to build cuvid and nvenc.

Please refer to the NVIDIA [Video developer zone][1] for the latest version and
examples and guides, this package is just provided for convenience since the
license for the headers allows that.

The package is tested to work with [Libav](https://libav.org) and [rust-av](https://github.com/rust-av/nvidia-video-codec-rs).

## Dependencies
- Recent NVIDIA drivers
  - Windows: Driver version 368.69  or higher
  - Linux:   Driver version 367.35  or higher

- Recent [CUDA toolkit][2]
  - CUDA 7.5

## Requirements

NVIDIA Kepler/Maxwell/Pascal based GPU, refer to the NVIDIA [Video developer zone][1]
for the specific models that support Encoding and Decoding.

[1]: https://developer.nvidia.com/nvidia-video-codec-sdk
[2]: http://developer.nvidia.com/cuda/cuda-toolkit

## Usage

Since CUDA provides an older version of the cuvid headers make sure to always give priority to the Video SDK headers, e.g.:

```
CPPFLAGS="-I/opt/nvidia-video-sdk/include -I/opt/cuda/include"
```
