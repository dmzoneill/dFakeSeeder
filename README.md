<!-- markdownlint-disable MD041 -->
![DFakeSeeder screenshot](https://github.com/dmzoneill/dFakeSeeder/blob/main/d_fake_seeder/images/dfakeseeder.png)

# D' Fake Seeder

- This is a Python GTK4 app very much under active development
- Obviously supported multiple torrents
- only supporting tcp/http at this time, but i have UDP in the works
- Based off of deluge, hense "D' Fake Seeder", but also a colloquialism for 'the'.
- Recently upgraded it from gtk3 to gtk4 so some functionality is under flux/might be buggy.

## How to run
- Use make
```bash
make run-debug
```

## Todo
- loads of stuff, deb, rpms, pypi, docker build
- need to fix requiremnts.txt/piplock and convert the solution to venv.
- fix a chunk of small bugs and finish some of the toolbar and other options.
- Udp
- Better user feedback
- All PR's welcome


![DFakeSeeder screenshot](https://github.com/dmzoneill/dFakeSeeder/blob/main/d_fake_seeder/images/screenshot.png)

## Typical setup
```text
{
    "upload_speed": 50,
    "download_speed": 500,
    "total_upload_speed": 50,
    "total_download_speed": 500,
    "announce_interval": 1800,
    "torrents": {
    },
    "http_headers": {
        "Accept-Encoding": "gzip",
        "User-Agent": "Deluge/2.0.3 libtorrent/2.0.5.0"
    },
    "agents": [
        "Deluge/2.0.3 libtorrent/2.0.5.0",
        "qBittorrent/4.3.1",
        "Transmission/3.00",
        "uTorrent/3.5.5",
        "Vuze/5.7.6.0",
        "BitTorrent/7.10.5",
        "rTorrent/0.9.6"
    ],
    "proxies": {
        "http": "",
        "https": ""
    },
    "columns": "",
    "concurrent_http_connections": 2,
    "concurrent_peer_connections": 10,
    "cellrenderers": {
        "progress": "Gtk.CellRendererProgress"
    },
    "textrenderers": {
        "total_uploaded": "humanbytes",
        "total_downloaded": "humanbytes",
        "session_uploaded": "humanbytes",
        "session_downloaded": "humanbytes",
        "total_size": "humanbytes",
        "announce_interval": "convert_seconds_to_hours_mins_seconds",
        "next_update": "convert_seconds_to_hours_mins_seconds",
        "upload_speed": "add_kb",
        "download_speed": "add_kb",
        "threshold": "add_percent"
    },
    "threshold": 30,
    "tickspeed": 3,
    "editwidgets": {
        "active": "Gtk.Switch",
        "announce_interval": "Gtk.SpinButton",
        "download_speed": "Gtk.SpinButton",
        "next_update": "Gtk.SpinButton",
        "session_downloaded": "Gtk.SpinButton",
        "session_uploaded": "Gtk.SpinButton",
        "small_torrent_limit": "Gtk.SpinButton",
        "threshold": "Gtk.SpinButton",
        "total_downloaded": "Gtk.SpinButton",
        "total_uploaded": "Gtk.SpinButton",
        "upload_speed": "Gtk.SpinButton"
    },
    "issues_page": "https://github.com/dmzoneill/DFakeSeeder/issues",
    "website": "https://github.com/dmzoneill/DFakeSeeder/",
    "author": "David O Neill",
    "copyright": "Copyright {year}",
    "version": "0.0.11",
    "logo": "images/dfakeseeder.png"
}
```