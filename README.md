<div align="center">

![Logo](https://nolus.explorers.guru/chains/nolus.png)

<h1>Nolus SnapShot</h1>


</div>

<div>
<i>We take node snapshot every day at 10:00 UTC
You can browse the logs for current snapshot date, block height, and file size information.</i>
</div>


  ##### Stop your node
`sudo systemctl stop nolusd`
##### Reset your node
This will erase your node database. If you are already running validator, be sure you backed up your priv_validator_key.json prior to running the the command.

`nolusd unsafe-reset-all --home $HOME/.nolus --keep-addr-book`
##### Download & Install the snapshot
`curl -L http://135.181.222.185/nolus/nolus-rila_latest.tar | tar -xf - -C $HOME/.nolus `
##### Restart Service & Check Log:
`sudo systemctl start nolusd && journalctl -u nolusd -f --no-hostname -o cat`
