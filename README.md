# Chiaki builds for Mac OS with old SDL support.

You may need to install brew and xcode dev tools.
```
xcode-select --install
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

You can try to compile it. You might need to install some libraries or remove.
```
git clone --recurse-submodules https://git.sr.ht/~thestr4ng3r/chiaki

brew install sdl2 cmake make protobuf openssl qt@5 pkg-config ffmpeg

cd chiaki && mkdir build && cd build
export CMAKE_PREFIX_PATH=$(brew --prefix qt@5)
cmake .. -DOPENSSL_ROOT_DIR=/opt/homebrew/opt/openssl -DOPENSSL_LIBRARIES=/opt/homebrew/opt/openssl/lib -DCHIAKI_GUI_ENABLE_SDL_GAMECONTROLLER=ON
```

# About Chiaki
Chiaki created by Florian Märkl
Official releases:
[https://git.sr.ht/~thestr4ng3r/chiaki](https://git.sr.ht/~thestr4ng3r/chiaki)
