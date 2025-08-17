# FlashInfer Pre-compiled Wheels

This repository contains pre-compiled FlashInfer wheels with AOT (Ahead-Of-Time) kernels.

## CUDA Architectures Support
These wheels were compiled with support for the following CUDA architectures:
- **TORCH_CUDA_ARCH_LIST="8.0 8.9 9.0a"**
 - **8.0**: NVIDIA A100, DGX A100
 - **8.9**: NVIDIA L4, NVIDIA RTX 4090, RTX 4080, RTX 4070 Ti, RTX 4070, RTX 4060 Ti, RTX 4060
 - **9.0a**: NVIDIA H100, H800 (Ada Lovelace architecture)

## Available Versions
- CUDA 12.6: Available in releases

## Usage

### In Dockerfile
```dockerfile
curl -L -o flashinfer.whl \
   "https://github.com/Sami-Fino/flashinfer-wheels/releases/download/v1.0.0-cuda126/flashinfer_python-0.2.11.post3-cp39-abi3-linux_x86_64.whl"
uv pip install flashinfer.whl --no-deps
