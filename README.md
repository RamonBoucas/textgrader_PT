# textgrader

## Overview
 

## Rules and guidelines
 

## How to install dependencies
 
 

## How to run your Kedro pipeline

You can run your Kedro project with:

```
kedro run --pipeline textgrader
```


### JupyterLab
To use JupyterLab, you need to install it:

```
pip install jupyterlab
```

You can also start JupyterLab:

```
kedro jupyter lab
```

### IPython
And if you want to run an IPython session:

```
kedro ipython
```

### Conjuntos de texto

O conjunto de textos trabalhado contém cerca de 170 temas, não há uniformidade nos nomes dos conceitos avaliados e na escala numérica dos conceitos, por isso agrupamos os temas em três grupos diferentes que possuirão conceitos diferentes e escalas numéricas diferentes

Primeiro conjunto de texto – temas 1 até 85 (cada conceito de  0 a200)
•	'Domínio da modalidade escrita formal',                                                                                                  
•	'Compreender a proposta e aplicar conceitos das várias áreas de conhecimento para desenvolver o texto dissertativo-argumentativo em prosa',   
•	'Selecionar, relacionar, organizar e interpretar informações em defesa de um ponto de vista',                                                 
•	'Conhecimento dos mecanismos linguísticos necessários para a construção da argumentação',                                                     
•	'Proposta de intervenção com respeito aos direitos humanos'           
Segundo conjunto de texto -  temas 86 até 137 (cada conceito de 0 a 10)
•	'Conteúdo',                                                                                                                               
•	'Estrutura do texto',                                                                                                               
•	'Estrutura de ideias',                                                                                                                 
•	'Vocabulário',                                                                                                                       
•	'Gramática e ortografia' 
Terceiro conjunto de texto - temas 137 – 170 (cada conceito de 0 a 10)
•	'Adequação ao Gênero Textual',                                                                                                               
•	'Adequação à modalidade padrão da língua',                                                                                                    
•	'Coesão e Coerência'
•	'Adequação ao Tema',                                                                                                                        
•	'Adequação e Leitura Crítica da Coletânea',                                                                                                











### How to convert notebook cells to nodes in a Kedro project
You can move notebook code over into a Kedro project structure using a mixture of [cell tagging](https://jupyter-notebook.readthedocs.io/en/stable/changelog.html#cell-tags) and Kedro CLI commands.

By adding the `node` tag to a cell and running the command below, the cell's source code will be copied over to a Python file within `src/<package_name>/nodes/`:

```
kedro jupyter convert <filepath_to_my_notebook>
```
> *Note:* The name of the Python file matches the name of the original notebook.

Alternatively, you may want to transform all your notebooks in one go. Run the following command to convert all notebook files found in the project root directory and under any of its sub-folders:

```
kedro jupyter convert --all
```

### How to ignore notebook output cells in `git`
To automatically strip out all output cell contents before committing to `git`, you can run `kedro activate-nbstripout`. This will add a hook in `.git/config` which will run `nbstripout` before anything is committed to `git`.

> *Note:* Your output cells will be retained locally.


