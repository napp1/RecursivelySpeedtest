# Recursively Speedtest
## Launch speedtest, recursively, every X seconds, and write results on CSV file.

Before install speedtest-cli (https://github.com/sivel/speedtest-cli):
`pip install speedtest-cli`

At the same time consider uploading the results, for external consultations, to an FTP space:
`while true; do curl -v -T speedtest.csv ftp://user:password@ftp.server.xx/dir/; sleep 1800; done`
