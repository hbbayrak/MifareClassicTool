########################################################################
# MIFARE CLASSIC TOOL DUMP TO PROXMARK EMULATOR - Clone initializer    #
########################################################################

The script "mct-dump2prox-emu" initializes the Mifare Classic emulator
of the Proxmark3 with the data of a dump like the MCT-App generates.
It is an easy way to create a real clone (with UID) of the Mifare
Classic tag you read with the MCT-App.

Dependencies:
- expect
- Proxmark3's client binary ;)

########################################################################

Usage: ./mct-dump2prox-emu <dump-file> <proxmark3-client-bin>
The script may need root privileges.

dump-file:
  The dump file is a file that was generated via the MCT-App.
  This is done by reading a full tag and then saving whole data.
  It should look like the "example-dump-file.txt".
  You can find the files in "MifareClassicTool/dump-files/" of your
  external storage (SD-Card).

proxmark3-client-bin:
  The client binary for communicating with the Proxmark3 is
  typically located in the "client" directory of your proxmark3-svn.
  It is simply called "proxmark3".

Usage Examples:
  ./mct-dump2prox-emu tag-to-clone.dump \
    proxmark-read-only/client/proxmark3

########################################################################





