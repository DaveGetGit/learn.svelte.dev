<script>
    let name = 'Svelte';
    let src = "./0266554465.jpeg";
    let string = 'This is a sample <steong>string</strong>';
        let count = 0;

    // $:if(count > 10){
    //     alert('count is high');
    //     count=0;
    // }

    $: doubled = count *2;

    function Increment(){
        count += 1;
    }
 
</script>

<h1>Hello {name.toUpperCase()}!</h1>

<p> component specific styling</p>

<!-- Dynamic Attributes -->
<img {src} alt="A Bird" />

<style>
    p{
        color:red;
        font-family:'Courier New', Courier, monospace;
        font-size:3em;
    }
</style>
<!-- Component names are always capitalised, to distinguish them from HTML elements. -->
<!-- HTML TAGS   NO SANITIZATION-->
<p>{@html string}</p>

<button on:click={Increment} class='primary'>
Click {count} {count === 1 ? 'time' : 'times'}   
{doubled}
</button>


<!-- If BLOCKs -->
{#if count > 10}
{count} is greater than 10.
{/if}





