# ccminer for ARMv8 CPUS

Based on https://github.com/monkins1010/ccminer/tree/ARM

Git and Build Process:
```bash
sudo apt-get install software-properties-common
sudo wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | sudo apt-key add -
sudo add-apt-repository 'deb http://apt.llvm.org/focal/ llvm-toolchain-focal-11 main'
sudo apt-get update
sudo apt-get install libcurl4-openssl-dev libssl-dev libjansson-dev automake autotools-dev build-essential -y
sudo apt-get install -y libllvm-11-ocaml-dev libllvm11 llvm-11 llvm-16-dev llvm-11-doc llvm-11-examples llvm-11-runtime clang-11 clang-tools-11 clang-11-doc libclang-common-11-dev libclang-11-dev libclang1-11 clang-format-11 python3-clang-11 clangd-11 clang-tidy-11 libclang-rt-11-dev libpolly-11-dev libfuzzer-11-dev lldb-11 lld-11 libc++-11-dev libc++abi-11-dev libomp-11-dev libclc-11-dev libunwind-11-dev libmlir-11-dev mlir-11-tools flang-11 libclang-rt-11-dev-wasm32 libclang-rt-11-dev-wasm64 libclang-rt-11-dev-wasm32 libclang-rt-11-dev-wasm64
sudo ln -sf /usr/lib/llvm-11/bin/clang-11 /usr/bin/clang
sudo ln -sf /usr/lib/llvm-11/bin/clang++ /usr/bin/clang++

git clone https://github.com/rizki0030/ccminer_arm.git
cd ccminer_arm
chmod +x build.sh
chmod +x configure.sh
chmod +x autogen.sh
CXX=clang++ CC=clang ./build.sh
```

For specific details on installing clang-16 on your current OS, check: https://apt.llvm.org/
