# SystemC & AccessNoxim
All you need to build and run SystemC and AccessNoxim on your system

building SystemC{do this inside systemc-2.3.1}

    export SYSTEMC_HOME=/usr/local/systemc231
    sudo mkdir $SYSTEMC_HOME
    chmod +x configure
    mkdir objdir
    cd objdir
    ../configure --prefix=$SYSTEMC_HOME
    make 
    sudo make install

building AccessNoxim{do this inside AccessNoxim_v0.3}

    export SYSTEMC_HOME=/usr/local/systemc231
    export SYSTEMC_HEADERS=$SYSTEMC_HOME/include
    export C_INCLUDE_PATH=$SYSTEMC_HEADERS
    export CPLUS_INCLUDE_PATH=$SYSTEMC_HEADERS
    cd bin
    make

to run AccessNoxim{do this inside AccessNoxim_v0.3/bin}

    chmod +x noxim
    ./noxim

you could run bashSetup.sh to add SYSTEMC_HOME and SYSTEMC_HEADERS and C_INCLUDE_PATH and CPLUS_INCLUDE_PATH permenantly to your .bash startup scrip

    chmod +x bashSetup.sh
    ./bashSetup.sh
