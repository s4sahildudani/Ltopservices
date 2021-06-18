<script>
    import Navbar from '../lib/components/__navbar.svelte'
     import Sidebar from '../lib/components/Sidebar.svelte'
    import Footer from '../lib/components/__footer.svelte'
</script>
<Navbar />
<Sidebar />
<slot></slot>

<Footer />