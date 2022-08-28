# Installation

    sudo curl -s https://raw.githubusercontent.com/amogusussy/torrentCLI/main/torrentcli -o /usr/bin/torrentcli && sudo chmod +x /usr/bin/torrentcli 

Alternatively, you can just download the script directly from the browser with the above link.

***

# Running

You can run it by typing `torrentcli search query`. So for example, if you were to want a Big Buck Bunny torrent, you could type `torrentcli Big Buck Bunny`

If you've downloaded it from the browser, you can run it with `python3 /path/to/torrentcli search query`

If you have [`vlc-bittorrent`](https://github.com/johang/vlc-bittorrent) installed, you can run the command with the `-s` flag to stream the torrent.

***

This is reliant on the [Librex](https://github.com/hnhx/librex/) API. \n
You can self host it yourself with the following commands:

    git clone https://github.com/hnhx/librex/
    cd librex
    php -S localhost:8080
    
Then open `/usr/bin/torrentcli` and replace `site = random.choice(sites)` with `site = 'http://localhost:8080'`


#Other Info
By default, this will use xdg-open, which is specific to the Xorg server on Unix-like machines. You can change that by editing `        subprocess.run(["xdg-open", magnet])` by replacing xdg-open with whatever torrent client you use.
