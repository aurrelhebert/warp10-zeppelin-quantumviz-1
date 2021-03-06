## Interpreter QuantumViz

This plugin can be used to plot quantumviz graphs or map with geoquantumviz. It use the library defined in quantum url given as parameter. 
To get started configure the QuantumViz interpreter, adding the url of the Quantum backend as parameter.
```
name:                 value:
warp10.url           http://localhost:8000/components
```

## Use
Just put the parameter in the paragraph quantumviz. One variable per line, multiple line will print multiple graphs.

```
%quantumviz
dataviz
data2
```

To work with quantum, data must be stored in the globale resource scope. In WarpScript, they can be set the following this sample: 
```
{
    'gts'
    [ 
        $gts1
        $gts2
    ]
    'params'
    [
        { 'key' 'key1' }
        { 'key' 'key2' 'color' ''#ff1010' }
    ]
    'globalParams'
    { 'interpolate' 'linear' }
}
```

## Set-up 

Compile the interpreter with maven.

```
mvn clean package
```

Create a directory quantumviz in folder interpreter.

Then copy the Jar with dependencies inside.

Stop and restart Zeppelin.
