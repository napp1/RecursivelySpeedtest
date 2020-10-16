# Recursively Speedtest
## Launch speedtest, recursively, every X seconds, and write results in CSV file.

First install speedtest-cli (https://github.com/sivel/speedtest-cli):

`pip install speedtest-cli`

Then launch the bash script `speedtest.sh` content:

`while true; do speedtest-cli --csv >> speedtest.csv; sleep 3600; done`

It just runs speedtest-cli every X seconds (3600 i.e.) and saves the results in CSV file.

The header of CSV file is: Server ID,Sponsor,Server Name,Timestamp,Distance,Ping,Download,Upload,Share,IP Address.


At the same time consider uploading the results, for external consultations, to an FTP space:

`while true; do curl -v -T speedtest.csv ftp://user:password@ftp.server.xx/dir/; sleep 1800; done`
