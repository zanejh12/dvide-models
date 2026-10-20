# dvide-models

ONNX models that [Dvide](https://github.com/zanejh12/dvide), a personal image compressor, downloads
on first use for AI upscaling. Each file is an ONNX export of the official
[Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) weights. The weights are unchanged; only
the format is converted (opset 17, dynamic height and width, fp32 and fp16).

Real-ESRGAN is © 2021 Xintao Wang, BSD 3-Clause; see `LICENSE-Real-ESRGAN`.

Release `realesrgan-v1`:

| File | Source weights | Bytes | SHA-256 |
|---|---|---|---|
| realesrgan-x4plus.onnx | RealESRGAN_x4plus.pth (v0.1.0) | 67,051,636 | 1dd781a70b7e849b473bf8cdb801f8cf1abfc42438de313048227691a854a3d3 |
| realesrgan-x4plus.fp16.onnx | same, fp16 | 33,654,926 | c143f59eb8ca52e76f58a2d3f45b1ba8f40323d93069f73aec2acc8db9084f76 |
| realesrgan-x4plus-anime-6b.onnx | RealESRGAN_x4plus_anime_6B.pth (v0.2.2.4) | 17,939,961 | 53d8d90bcc349633c5be8f4fef8e63fc009a1b1ec2a4a0e85217e5f95afa917b |
| realesrgan-x4plus-anime-6b.fp16.onnx | same, fp16 | 9,004,211 | 78bc25b856373f652d297aec1d8d3115643a4f8300796e39b6d9d799eca55b20 |

Input `input` and output `output`: NCHW float RGB in [0, 1]; the output is 4x larger.
