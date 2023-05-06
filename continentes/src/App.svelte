<script>
    import { blank_object } from "svelte/internal";

  let continentes = ["Africa","America","Europa","Asia","Oceania"]
    let valor=""
       const Oceania=[
        "Australia",
        "Fiyi",
        "Kiribati",
        "Islas Marshall",
        "Islas Salomón",
        "Micronesia",
        "Nauru",
        "Nueva Zelanda",
        "Palaos",
        "Papúa Nueva Guinea",
        "Samoa",
        "Tonga",
        "Tuvalu",
        "Vanuatu"
       ]
       
       const Asia=[
        "Japon",
        "China",
        "Corea del Sur",
        "Corea del Norte",
        "Filipinas",
        "Iraq",
        "Pakistan",
        "India",
        "Bangaldesh",
        "Israel"
       ]

       const Africa=[
        "Egipto",
        "Sud-África",
        "Marruecos",
        "Uganda",
        "Nigeria",
        "Zimbaue",
        "Libia"
       ]

       const Europa=[
      "Paises:",
      "Alemania",
      "España",
      "Francia",
      "Italia",
      "Dinamarca",
      "Paises Bajos"
    ]
  
    const America=[
      "Estados Unidos",
      "Canada",
      "Cuba",
      "Argentina",
      "Colombia",
      "Mexico",
      "Uruguay",
      "Brasil"
    ]

</script>

<style>
  div{
    width:190px;
    height:100vh;
    
   
  }
  p{
    font-size:14px;
  }
  img{
    position:absolute;
    
    top: 40px; left: 300px;
   
  }

</style>

<svelte:head>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>
</svelte:head>

<svelte:body id="body"/>
<select class="bg-primary text-white" bind:value={valor}>
  {#each continentes as v}
  <option value={v}>{v}</option>
  {/each}
</select>

{#if valor == "Africa"}
<img class="border border-primary" src="https://cdn.pixabay.com/photo/2014/04/02/16/24/map-307196_1280.png" width="450px" alt="mapa">
<div class="bg-dark text-white">
<strong>Has selecionado Africa</strong>
<h1></h1>
<h6>Paises de Africa:</h6>
{#each Africa as re}
<p >-{re}</p>
{/each}
</div>

{:else if valor=="America"}
<img class="border border-primary" src="https://cdn.pixabay.com/photo/2018/03/14/18/35/americas-3225976_1280.png" width="400px" alt="mapa">
<div class="bg-dark text-white">
<strong>Has puesto america</strong>
<h1></h1>
<h6>Paises de America:</h6>
{#each America as er}
<p>-{er}</p>
{/each}
</div>

{:else if valor=="Europa"}
<img class="border border-primary" src="https://cdn.pixabay.com/photo/2014/03/25/16/27/europe-297168_640.png" width="400px" alt="mapa">
<div class="bg-dark text-white">
<strong>Europa: </strong>
<h1> </h1>
<h6>Paises de Europa:</h6>
{#each Europa as er}
<p>-{er}</p>
{/each}
</div>

{:else if valor=="Asia"}
<img class="border border-primary" src="https://cdn.pixabay.com/photo/2014/04/02/16/24/map-307197_1280.png" width="450px" alt="mapa">
<div class="bg-dark text-white">
<strong>Has puesto Asia</strong>
<h1> </h1>
<h6>Paises de Asia:</h6>
{#each Asia as rere}

<p>-{rere}</p>
{/each}
</div>

{:else if valor=="Oceania"}
<img class="border border-primary" src="https://cdn.pixabay.com/photo/2021/07/15/12/55/blank-australia-map-6468420_1280.png" width="450px" alt="mapa">

<div class="bg-dark text-white">
<strong>Has puesto oceania</strong>
<h1></h1>
<h6>Paises de Oceania:</h6>
{#each Oceania as zaza}
<p>-{zaza}</p>
{/each}

</div>



{:else}
<div class="bg-dark text-white">
<p>No has puesto nada</p>
</div>
{/if}



