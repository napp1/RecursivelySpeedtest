# Recursively Speedtest
## Launch speedtest, recursively, every X seconds, and write results on CSV file.

First install speedtest-cli (https://github.com/sivel/speedtest-cli):

`pip install speedtest-cli`

`speedtest.sh` just execute it every X seconds (3600 i.e.):

`while true; do speedtest-cli --csv >> speedtest.csv; sleep 3600; done`


At the same time consider uploading the results, for external consultations, to an FTP space:

`while true; do curl -v -T speedtest.csv ftp://user:password@ftp.server.xx/dir/; sleep 1800; done`
