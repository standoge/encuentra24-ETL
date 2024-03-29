# Encuentra 24 ETL

ETL process for Encuentra24 El Salvador with `Selenium` to extract data about car announcements and after be transformed
with `Pandas`.

Project is separated in three. A notebook for extraction with Selenium which use a `xpath.yml` file
where are defined the `xpath` sentences to use to extract required data to create the dataframes. Another with the
transformations to apply to the data extracted.
And the last one with the functions required to create entities like a star model for a Warehouse.

> `persistence` directory has the outputs from `Extraction` and `Loading` notebooks.

## Extraction :brain:

Here is the code to extrac the data.

* Includes init instructions (dependencies, global configurations)
* Functions section, where are defined all functions used.
* Relevant cell has its respective text to explain what is happening.

## Transformation :moon:

Here is the code to check and fix data inconsistencies.

* Functions section, where are defined all functions used.
* Transformations required are explained, with a subtitle and description to explain what was the transformation
  applied.

> This notebook is not required to be executed, just execute it if you data extracted from `Extraction` notebook has some of the
> problems described in the notebook.

## Load :chart:

Here data are split to follow a star model using `bottom-down` architecture.

```mermaid

erDiagram

    dim_model {
        model_ia
        model
    }
    
    dim_description {
        description_id
        description
    }
    
    dim_engine {
        engine_id
        engine
    }
    
    fact_sedan_stats {
        fact_id
        year
        kilometers
        price
        model_id
        engine_id
    }
```


---
:bamboo: ~
