# ModularCR
A module-based cognitive radio implementation for easy testing of machine learning techniques in the spectrum decision phase

### Environment
  
  * SO: Antergos Linux 19.1 64 bits
  * Package manager:
    * pacman (default from arch community)
    * yay ( for user repository, such as AUR: [https://aur.archlinux.org/])
  
### First Steps

1. Installing GNURadio and 802.11:

* You can install any version of GNURadio between ]3.7.\*,3.8] however, 3.8+ will not work with this tutorial.
  
* gr_foo is required to work with some gr_80211 blocks:
  
  * Before the installation begin with these 2 dependencies of gr-foo
  
        sudo pacman -S boost
        sudo pacman -S swig
  
  * Finally, install gr_foo

        git clone --single-branch --branch maint-3.7 https://github.com/bastibl/gr-foo.git
        cd gr-foo
        mkdir build
        cd build
        cmake ..
        make
        sudo make install
        sudo ldconfig

* And now the 802.11:

        git clone --single-branch --branch maint-3.7 https://github.com/bastibl/gr-ieee802-11.git
        cd gr-ieee802-11
        mkdir build
        cd build
        cmake ..
        make
        sudo make install
        sudo ldconfig

* Also install this last 2 dependences of gnuradio:
      
        pip2.7 install lxml
        pip2.7 install cheetah
        
1. If you reach here without problems, just type the command below and start coding:

        gnuradio-companion
       
