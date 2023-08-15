<script setup>
import Navbar from "./components/Navbar.vue";
import Dashboard from "./components/Dashboard.vue";
import DasboardItemCard from "./components/DasboardItemCard.vue";
import LeadingEdge from "./components/LeadingEdge.vue";
import CommuniTraders from "./components/CommunityTrade.vue";
import FooterTrade from "./components/FooterTrade.vue";
</script>

<template>
  <header class="bg-really sticky top-0">
    <Navbar />
  </header>
  <main>
    <Dashboard />
    <DasboardItemCard />
    <LeadingEdge />
    <CommuniTraders />
  </main>
  <footer class="bg-graydark">
    <FooterTrade />
  </footer>
</template>
