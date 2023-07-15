## Afrineuron Code-interpreter
 
Check out our projects portifolio at https://afrineuron.com/

An open source implementation of OpenAI's ChatGPT [Code interpreter](https://openai.com/blog/chatgpt-plugins#code-interpreter).

Simply ask the OpenAI model to do something and it will generate & execute the code for you.


## Installation

Open a terminal and run:

```
cd frontend
run mpm run dev
cd ..
pip install gpt-code-ui
gptcode
```

In order to make basic dependencies available it's recommended to run the following `pip` install
in the Python environment that is used in the shell where you run `gptcode`:

```sh
pip install "numpy>=1.24,<1.25" "dateparser>=1.1,<1.2" "pandas>=1.5,<1.6" "geopandas>=0.13,<0.14" "PyPDF2>=3.0,<3.1" "pdfminer>=20191125,<20191200" "pdfplumber>=0.9,<0.10" "matplotlib>=3.7,<3.8"
```
 
## Features
- File upload
- File download
- Context awareness (it can refer to your previous messages)
- Generate code
- Run code (Python kernel)
- Model switching (GPT-3.5 and GPT-4)

## Misc.
### Using .env for OpenAI key
You can put a .env in the working directory to load the `OPENAI_API_KEY` environment variable.

### Configurables
Set the `API_PORT`, `WEB_PORT`, `SNAKEMQ_PORT` variables to override the defaults.

Set `OPENAI_BASE_URL` to change the OpenAI API endpoint that's being used (note this environment variable includes the protocol `https://...`).

You can use the `.env.example` in the repository (make sure you `git clone` the repo to get the file first).

### Docker
[localagi](https://github.com/localagi) took the effort of bundling the Python package in a Docker container. Check it out here: [gpt-code-ui-docker](https://github.com/localagi/gpt-code-ui-docker).


