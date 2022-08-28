# Installation

    sudo curl -s https://raw.githubusercontent.com/amogusussy/torrentCLI/main/torrentcli -o /usr/bin/torrentcli && sudo chmod +x /usr/bin/torrentcli 

***

# Running

You can run it by typing `torrentcli search query`. So for example, if you were to want a Better Call Saul torrent, you could type `torrentcli Better Call Saul`

If you have [`vlc-bittorrent`](https://github.com/johang/vlc-bittorrent) installed, you can run the command with the `-s` flag to stream the torrent.

***

This is reliant on the [Librex](https://github.com/hnhx/librex/) API. You can self host it yourself with the following commands:

    git clone https://github.com/hnhx/librex/
    cd librex
    php -S localhost:8080
    
Then open `/usr/bin/torrentcli` and replace `site = random.choice(sites)` with `site = 'http://localhost:8080'`
