# ![Uploadrr by CvT](https://i.ibb.co/2NVWb0c/uploadrr.webp)

I have no clue what I'm doing so thought I'd fork it, bork it and, duct tape it back together to get people to sing my praises. 
Hopefully it works and makes your life simplier.

## What It Can Do:
  - Generates and Parses MediaInfo/BDInfo.
  - Generates and Uploads screenshots.
  - Uses srrdb to fix scene filenames
  - Can grab descriptions from PTP (automatically on filename match or arg) / BLU (arg)
  - Obtains TMDb/IMDb/MAL identifiers.
  - Converts absolute to season episode numbering for Anime
  - Generates custom .torrents without useless top level folders/nfos.
  - Can re-use existing torrents instead of hashing new
  - Generates proper name for your upload using Mediainfo/BDInfo and TMDb/IMDb conforming to site rules
  - Checks for existing releases already on site
  - Manual or Automated Queuing 
  - Adds to your client with fast resume, seeding instantly (rtorrent/qbittorrent/deluge/watch folder)
  - ALL WITH MINIMAL INPUT!
  - Currently works with .mkv/.mp4/Blu-ray/DVD/HD-DVDs (or anything if --full-directory is applied)

## Supported Sites

|      |      |      |     |      |      |     |      |
|------|------|------|-----|------|------|-----|------|
| ACM  | AITHER | ANT | BHDTV | BLU | CP2P | FL | FNP |
| HDB  | HDT | HUNO | JPTV | LCD | LDU | LST | LT |
| MTV  | NBL  | OE | OTW | PTER | PTT | R4E | RF |
| RTF  | SN | STC | STT | TDC | TL | TTG | TTR |
| ULCX | UTP |






## Coming Soon:
  - Better support for FANRES + ADULT Content 

  

## **Setup:**
   - **REQUIRES AT LEAST PYTHON 3.7 AND PIP3**
   - Needs [mono](https://www.mono-project.com/) on linux systems for BDInfo
   - Also needs MediaInfo and ffmpeg installed on your system
      - On Windows systems, ffmpeg must be added to PATH I recomend using https://scoop.sh/ , alternatively follow this guide for manual installation (https://windowsloop.com/install-ffmpeg-windows-10/) 
      - On linux systems, get it from your favorite package manager
      - On Mac OS either install in brew, or get static builds and place in `/usr/bin` or (better practice) create your own bin ex:`$HOME/.local/bin` then edit `$HOME/.zshrc` by adding export `PATH="$PATH:$HOME/.local/bin"`
   - Clone the repo to your system `git clone https://github.com/z-ink/Uploadrr.git`
   - Copy and Rename from `data/backup/example-config.py` to `data/config.py`
   - Edit `config.py` to use your information (more detailed information in the [wiki](https://github.com/L4GSP1KE/Upload-Assistant/wiki))
      - tmdb_api (v3) key can be obtained from https://developers.themoviedb.org/3/getting-started/introduction
      - image host api keys can be obtained from their respective sites
   - Install necessary python modules `pip3 install --user -U -r requirements.txt`
     
   

## **Updating:**
  - To update first navigate into the Upload-Assistant directory: `cd Upload-Assistant`
  - Run a `git pull` to grab latest updates
  - Run `python3 -m pip3 install --user -U -r requirements.txt` to ensure dependencies are up to date
## **CLI Usage:**
  
  `python3 upload.py "/downloads/path/to/content" --args`
  
  Args are OPTIONAL, for a list of acceptable args, pass `--help`
## **Docker Usage:**
  Personally untested, but Rx69 gave them files. Hopefully it works for you! Otherwise try checking [docker usage wiki page](https://github.com/L4GSP1KE/Upload-Assistant/wiki/Docker) for inspiration. 
