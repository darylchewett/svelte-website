<script>
  import "../app.scss";
  import Navbar from "../components/navbar.svelte";
  import Footer from "../components/footer.svelte";
</script>

<div class="non-bs-container">
<Navbar class="page-header" />

<slot class="page-content" />

<Footer class="page-footer" />
    </div>

<style>
    
    .non-bs-container{
        display: flex;
        flex-direction: column;
        height: 100dvh;
    }
    
    .page-content{
        flex: 1 0 auto;
        text-align: center !important;
        margin: auto;
       
    }
    
    .page-header{
        height: 50px;
        flex-shrink: 0;
    }
    
    .page-footer{
        height: 30px;
        flex-shrink: 0;
    }
</style>