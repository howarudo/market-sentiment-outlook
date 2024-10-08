# Financial Concepts

## Demo
Demo of the app released through streamlit! [CLICK HERE](https://financial-concepts.streamlit.app/)

## Tech Stack
- Dependency Management: **poetry**
- Deployment: **Docker**, **streamlit**
- Web Scraping: **BeautifulSoup**
- Data Visualization: **plotly**

## Setup
Docker is needed for setup. [Docker](https://docs.docker.com/get-started/get-docker/) can be downloaded here. Environment inside docker is setup using poetry. This ensures that any machine with docker will be compatible.

1. Build image

```zsh
sh scripts/build.sh
```

2. Run image

```zsh
sh scripts/run.sh
```

3. Access docker container terminal

```zsh
docker exec -it financial-concepts-cnt bash
```


### Setting up Jupyter Lab Server

```bash
poetry run jupyter lab --allow-root --ip=0.0.0.0 --no-browser --port=8877 --NotebookApp.token='' --NotebookApp.password=''
```
This will start a jupyter lab server at `localhost:8877`

### Running Streamlit Demo

```bash
poetry run streamlit run --server.port=8878 src/Introduction.py
```
