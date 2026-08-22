# podcastinator
An HTTP listener backend as a reverse-proxy target for "/*.rss" URIs under Caddy.

# Installation
Podcastinator is build to run as a reverse-proxy backend with Caddy doing ALL the heavy lifting involving creating and maintaining SSL certs (automatically!) and serving static files (e.g. HTML files that present your RSS feed links on a nice browser page).

Follow [instructions for installing Caddy](https://caddyserver.com/docs/install).

After Caddy, everything else installed under a Python virtual environment.

For a production installation, you just need these commands.
"""shell
mkdir ~/projects
cd ~/projects
git clone https://github.com/jeffclough/podcastinator.git
cd podcastinator
python3 -m venv .venv
source .venv/bin/activate
pip install \
    "fastapi[standard]" 
    uvicorn \
    python-json-logger
"""

If you're interested in updating the code, it's almost the same.
"""shell
mkdir ~/projects
cd ~/projects
git clone https://github.com/jeffclough/podcastinator.git
cd podcastinator
python3 -m venv .venv
source .venv/bin/activate
pip install -e \
    "fastapi[standard]" 
    uvicorn \
    python-json-logger \
    ".[dev]"
"""


