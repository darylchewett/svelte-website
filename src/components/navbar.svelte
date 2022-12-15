<script>
    import {page} from "$app/stores";
    import {goto} from "$app/navigation";
</script>

<div class="navbar-container">
    <button class="navbar-link"
         on:click={() => goto('/')}
         class:active={$page.url.pathname==='/'}>
       <h3> Home </h3>
    </button>
    <button class="navbar-link"
         on:click={() => goto('/about')}
         class:active={$page.url.pathname==='/about'}>
       <h3> About </h3>
    </button>
    <button class="navbar-link"
         on:click={() => goto('/coding')}
         class:active={$page.url.pathname==='/coding'}>
        <h3>Code Projects</h3>
    </button>
    <button class="navbar-link"
         on:click={() => goto('/photography')}
         class:active={$page.url.pathname==='/photography'}>
        <h3>Photography</h3>
    </button>
    <button class="navbar-link"
         on:click={() => goto('/contact')}
         class:active={$page.url.pathname==='/contact'}>
        <h3>Contact</h3>
    </button>

</div>


<style>
    .navbar-container {
        height: 50px;
        width: 100dvw;
        background-color: #222222;
        display: flex;
        text-align: center;
    }
    
    .navbar-link {
        height: 50px;
        border: 3px solid black;
        background-color: #222222;
        color: white;
        width: 20dvw;
        flex: 1;
    }
    
    .navbar-link:hover {
        background-color: #333333;
    }
    
    .active {
        background-color: #444 !important;
        
        border-bottom: none;
    }

    h3{
        margin-top:5px;
        -webkit-user-select: none; /* Safari */
        -moz-user-select: none; /* Firefox */
        -ms-user-select: none; /* IE10+/Edge */
        user-select: none; /* Standard */
    
    }
    
</style>