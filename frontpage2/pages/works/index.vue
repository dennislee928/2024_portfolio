<template>
  <div>
    <Header />
    <div class="page-title">
      <h1>Works</h1>
    </div>
    <div class="grid-container">
      <WorkCard
        project_name="2023portfolio"
        project_title="Front-end developer"
        github_link="https://github.com/dennisleeNCCUDCT/DennisLEEportfolio2024"
        website_link="https://2023dennislee3dportfolio.netlify.app"
        background_image="https://2023dennislee3dportfolio.netlify.app/"
      />
      <WorkCard
        project_name="Image<->Audio transfer"
        project_title="Full stack developer"
        github_link="https://github.com/dennisleeNCCUDCT/help_transfer_cryptos"
        website_link="https://help-transfer-cryptos-front-page.pages.dev/"
        background_image="https://example.com/background.jpg"
      />
      <WorkCard
        project_name="Guitar Store"
        project_title="Front-end developer"
        github_link="https://github.com/dennisleeNCCUDCT/guitarstore"
        website_link="https://dennis-lee-guitar-store.netlify.app"
        background_image="https://example.com/background.jpg"
      />
      <WorkCard
        project_name="Education App"
        project_title="Unity developer"
        website_link="https://apps.apple.com/mm/app/%E5%B3%B6%E5%B6%BC%E9%81%8A%E6%88%B2-%E8%B3%AA%E6%95%B8%E8%88%87%E5%90%88%E6%95%B8/id6447821110"
        background_image="https://example.com/background.jpg"
      />

      <WorkCard
        project_name="Dynamic NFT"
        project_title="Unity developer"
        website_link="https://akaswap.com/akaobj/12650"
        background_image="https://example.com/background.jpg"
      />

      <WorkCard
        project_name="Meta hackthon"
        project_title="Spark AR developer"
        website_link="https://dct.nccu.edu.tw/PageDocAll/Detail?fid=12444&id=24820"
        background_image="https://example.com/background.jpg"
      />
      <WorkCard
        project_name="Smart Contract"
        project_title="Solidity developer"
        github_link="https://github.com/dennisleeNCCUDCT/NFT_Smart_Contract_1"
        website_link="https://dct.nccu.edu.tw/PageDocAll/Detail?fid=12444&id=24820"
        background_image="https://example.com/background.jpg"
      />

      <!-- More grid items can be added -->
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from "~/components/Header.vue";
import WorkCard from "~/components/WorkCard.vue";

export default {
  components: {
    Header,
    WorkCard,
  },
};
</script>

<style>
.page-title {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin-bottom: 20px;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* Adjust based on layout needs */
  gap: 20px; /* Space between grid items */
  padding: 20px;
  max-width: 1200px; /* Maximum width of the grid */
  margin: 0 auto; /* Center the grid horizontally within its parent */
  justify-content: center; /* Center grid items horizontally */
  align-items: start; /* Align grid items to the start vertically */
}

.grid-item {
  background-color: #ccc; /* For better visibility */
  padding: 20px;
  text-align: center; /* Center text within the grid item */
}

/* Responsive adjustments */
@media (max-width: 992px) {
  .grid-container {
    grid-template-columns: repeat(2, 1fr); /* Two columns for medium screens */
  }
}

@media (max-width: 768px) {
  .grid-container {
    grid-template-columns: 1fr; /* Single column for small screens */
    width: 100%; /* Full width on small devices */
    padding: 10px;
  }
}
</style>
