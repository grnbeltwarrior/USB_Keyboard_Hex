The original use of this script was to take leftover capture data from a pcap and put it into the USB Keyboard hex and decode it.

tshark -r 'data3.pcap' -T fields -e usb.capdata > data3.txt
cat data3.txt | cut -d':' -f 3 | grep -v '00' > data3_final.txt
