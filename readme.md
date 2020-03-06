# Test to produce error for googletest issue 2506

# Steps

1. build using cmake
2. `while (rm -f *.xml && ctest -j $(nproc) -Q && xmllint --noout *.xml); do sleep 0.1; done`

This will run in a loop until an invalid XML has been detected. As this is a test on a race condition it might take only a few seconds until minutes.
