# Looping In Svelte

## Syntax : 
```bash
    {#each array as item}
      <-- Code -->
    {/each}
```
### Let Consider Example : 
let colors =[
    {name:'red', hex:'#f00'},
    {name :'green', hex:'#0f0'},
    {name :'blue', hex:'#00f'},
    {name :'yellow', hex:'#ff0'},
]

```bash
   <ul>
    {#each colors as color}
        <li>{color.name}</li>
    {/each}
   </ul>
```

#### Name with Color
```bash
   <ul>
    {#each colors as color}
        <li style="color:{color.hex};" >{color.name}</li>
    {/each}
   </ul>
```

#### Destructure the color as name & hex
```bash
   <ul>
    {#each colors as { name, hex }}
        <li style="color:{hex};" >{name}</li>
    {/each}
   </ul>
```