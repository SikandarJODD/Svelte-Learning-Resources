# Looping In Svelte

## Syntax : 
```bash
    {#each array as item}
      <-- Code -->
    {/each}
```
### Let Consider Example : 
```
let colors =[ <br/>
      {name:'red', hex:'#f00'}, 
      {name :'green', hex:'#0f0'}, 
      {name :'blue', hex:'#00f'}, 
      {name :'yellow', hex:'#ff0'}, 
      {name : 'purple'}
]
```
### Each Name is Printed
```bash
   <ul>
    {#each colors as color}
        <li>{color.name}</li>
    {/each}
   </ul>
```

### Name with Color
```bash
   <ul>
    {#each colors as color}
        <li style="color:{color.hex};" >{color.name}</li>
    {/each}
   </ul>
```

### Destructure the color as name & hex
```bash
   <ul>
    {#each colors as { name, hex }}
        <li style="color:{hex};" >{name}</li>
    {/each}
   </ul>

```
### Fallback || Default Value for Black <code>Hex in Black </code>
<p>If there is no hex value it would be Purple by Default</p>

```bash
   <ul>
    {#each colors as { name, hex ='purple' }}
        <li style="color:{hex};" >{name}</li>
    {/each}
   </ul>
   
```

