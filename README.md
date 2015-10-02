# SPFLashTool

LINUX:

sudo apt-get install libusb-dev

sudo gedit /etc/udev/rules.d/80-persistent-usb.rules

SUBSYSTEM=="usb", ACTION=="add", ATTR{idVendor}=="0e8d", ATTR{idProduct}=="*"

sudo service udev restart

sudo gedit /etc/udev/rules.d/20-mm-blacklist-mtk.rules

ATTRS{idVendor}=="0e8d", ENV{ID_MM_DEVICE_IGNORE}="1"
ATTRS{idVendor}=="6000", ENV{ID_MM_DEVICE_IGNORE}="1"

sudo service udev restart
