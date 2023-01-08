# Great Expectations DQ from YAML
Great Expectations is a Python library to apply Data Quality checks in the data pipelines. Developers have to define context, data source and rules in Python to run them on supported datasets.

In this project we will try to define a YAML file with all the necessary rules and configurations and a Python library to automatically read the YAML and setup GE dynamically so that developers don't need to write code for defining rules. A kind of no-code approach.

## Sample YAML file

```yaml
suite_name:
    expectations:
        - rule: expect_column_values_to_be_unique
          args:
            column: column_name
            result_format: COMPLETE
          meta:
            description: Column values to be unique
            notes: Any information specific to this project
        
        - rule: expect_column_values_to_be_in_set
          args:
            column: column_name
            value_set: ['PS1', 'PS2', 'PS3']
            result_format: COMPLETE
          meta:
            description: Column values to be unique
            notes: Any information specific to this project

```
