# Jupyter Notdebook Typescript Playground

## Installation

- Ensure Python 3.x is installed (tslab may require Python < 3.11)

### Globally

- Install [Jupyter Nodebook](https://jupyter.org/install#jupyter-notebook):

```sh
pip install notebook
```

- After installing one of the following TypeScript kernels, its availability can be checked with

```sh
jupyter kernelspec list
```

and it can be selected in the Jupyter notebook.

#### With tslab

```sh
npm install -g tslab
tslab install
```

#### With itypescript

```sh
npm install -g itypescript
its --install=local
```

### Locally in this repository (which is probably preferable, but slightly more work)

- Update pip to ensure that it supports virtual environments:

```sh
pip install --upgrade pip
```

- Create the virtual Python environment:

```sh
python -m venv .venv
```

- Activate it in the current sh session:

```sh
source .venv/bin/activate
```

Checking `which python` will show whether the virtual environment is active. The activation will need to be done for each new sh session, but can be automatedcan be done automatically with a [small script](https://stackoverflow.com/a/50830617/6813271) or [tool](https://stackoverflow.com/a/52262697/6813271).

- Install [Jupyter Nodebook](https://jupyter.org/install#jupyter-notebook):

```sh
pip install notebook
```

- The following command may be required to install the IPython kerne into the virtual environment:

```sh
ipython kernel install --user --name=.venv
```

- Install tslab and itypescript locally with:

```sh
npm ci
```

- After installing one of the following TypeScript kernels, its availability can be checked with

```sh
jupyter kernelspec list
```

and it can be selected in the Jupyter notebook.

#### With tslab

- Install the tslab kernel locally:

```sh
npx tslab install
```

- The tslab kernel file definition (seen in `jupyter kernelspec list`) references `tslab` without path. You either need to add it to the `$PATH` or add an absolute path in that file.

#### With itypescript

```sh
npx its --install=local
```

## Visual Studio Code

- [Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
- [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python), which also allows activating virtual Python environments automatically in its internal terminals with the setting `Terminal: Activate Environment`.

## Example

- [Minimal Hello World Example](./hello-world.ipynb)
