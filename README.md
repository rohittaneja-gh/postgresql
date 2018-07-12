# postgresql
Helpful Postgresql queries

## General
* Escaping single quote (')
  > ''
* Aggregate values
  ````
  select array_agg( '''' || value || '''')
  ````
* Concatanate a string
  ````
  select concat( 'prefix' || value || 'suffix')
  ````
* Check if a fields exists in a json
  ````
  SELECT '{"key_a": {"nested_key": "a"}}'::jsonb -> 'key_a' ? 'nested_key' 
  ````
