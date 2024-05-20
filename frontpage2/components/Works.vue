<template>
  <div class="work">
    <!-- Project 1 -->

    <!-- Project 2 and 3 -->
    <div class="project2-3">
      <div class="title">
        <!-- Title for Projects 2 and 3 -->
        <p>Changes he made, and is going</p>
      </div>
      <div class="projects-container">
        <div class="left-side">
          <div class="project-image">
            <!-- Image for Project 2 -->
            <img src="../assets/2023portfolio.png" alt="Project 2 Image" />
          </div>
          <div class="project-1-text">
            <!-- Text for Project 2 -->
            <NuxtLink to="https://2023dennislee3dportfolio.netlify.app/">
              <p class="herf">
                Using react plus three.js to send oneself to space? Is it still
                possible in 2023?
              </p>
            </NuxtLink>
            <div class="warrant">
              <p>See this man?</p>
              <NuxtLink to="./warrant">
                <p class="contact">Contat us immediately!</p>
              </NuxtLink>
              <p>to get your rewards!</p>

              <p>Crimes:</p>

              <p>Unauthorized Time Travel: Serilously.</p>
            </div>
          </div>
        </div>
        <div class="center-side">
          <div class="nft-section">
            <div class="nft-text">
              <!-- NFT Text -->
              <p class="nft-info-text">
                First student creates dynamic
                <NuxtLink to="https://akaswap.com/akaobj/12650">
                  <p class="herf">NFT</p>
                </NuxtLink>
                in NCCU.
              </p>
            </div>
            <div class="nft-image">
              <!-- NFT Image -->
              <img src="../assets/nft.png" alt="NFT Image" />
            </div>
          </div>
          <div class="project-image">
            <!-- Image for Project 3 -->
            <img src="../assets/gtstore.png" alt="Project 3 Image" />
          </div>
          <div class="project-text">
            <!-- Text for Project 3 -->
            <p>
              Taiwan's first online guitar trading storefront: Did they finally
              get the license?
            </p>
            <NuxtLink to="https://dennis-lee-guitar-store.netlify.app/">
              <p class="herf">A 2 stage react project.</p>
            </NuxtLink>
          </div>
        </div>
        <div class="right-side">
          <!-- Reward Divs -->
          <div class="meta-image">
            <img src="../assets/meta.png" alt="Meta Image" />
          </div>
          <div class="meta-text">
            <NuxtLink
              to="https://dct.nccu.edu.tw/PageDocAll/Detail?fid=12444&id=24820"
            >
              <p class="herf">
                2023 Meta Taipei Hackathon Best Initiative Award:
              </p>
            </NuxtLink>
            <p>Changing the World with AR Is Not a Dream.</p>
          </div>
          <div class="edu-image">
            <img src="../assets/edu.png" alt="Edu Image" />
          </div>
          <div class="edu-text">
            <NuxtLink
              to="https://apps.apple.com/mm/app/nccuedu-vr/id1609854458"
            >
              <p class="herf">Promoter of video game education.</p>
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* 基礎樣式 */
.work {
  display: flex;
  font-family: "Old Newspaper Types", serif;
  margin: 5px;
  width: 100%;
  height: auto;
}

.project2-3 {
  /* Changed to column for consistency */
  width: 100%;
}

.projects-container {
  display: flex;
  flex-direction: row; /* Align all sections in a column */
  margin: 5px;
}

.title {
  font-size: max(2vw, 18px);
  margin-bottom: 10px;
}

/* Align sections side by side using flex */
.left-side,
.center-side,
.right-side {
  display: flex;
  flex-direction: column; /* Maintain column layout across all screens */
  width: 100%; /* Use full width for each section */
  margin: 10px;
}

.project-image,
.nft-image,
.meta-image,
.edu-image {
  width: 100%;
  padding-top: 56.25%; /* Adjust to aspect ratio of 16:9 */
  position: relative;
}

img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.project-text,
.nft-text,
.meta-text,
.edu-text {
  margin: 5px;
}

/* Adjust text styles for readability */
.herf {
  text-decoration: underline;
  font-size: 1.2rem; /* Larger font size for readability */
}
.warrant {
  border: 1px solid black;
  text-align: center;
  font-family: "Old Newspaper Types", serif;
  font-size: xx-small;
  /**/
  margin: 0;
  margin-right: 0px;
  margin-top: 5px;
  top: 50%;
  padding-left: 10px;
  padding-right: 10px;
}
.contact {
  text-decoration: underline;
}
/* 手機裝置的 CSS 媒體查詢 */
@media (max-width: 768px) {
  .left-side {
    width: 25%;
  }
  .project2-3 {
    flex-direction: column;
    width: 100%;
  }
  .center-side {
    width: 30%;
  }
  .right-side {
    width: 28%;
  }
  .title {
    font-size: 5vw; /* 增加字體大小使其在手機上更易於閱讀 */
  }

  .nft-section,
  .projects-container {
    flex-direction: row;
    flex-wrap: wrap;
  }

  .nft-image {
    height: 100%;
    width: 100%;
  }
  .nft-text {
    font-size: xx-small;
    height: 100%;
    width: 100%;
  }

  .nft-section {
    display: grid;
    grid-template-columns: 50% 50%;
    grid-template-columns: 0.5fr 2fr;
    margin-bottom: 10px;
  }
  .nft-info-text {
    width: auto;
  }
  .meta-text {
    font-size: x-small;
  }
  .project-1-text {
    font-size: x-large;
  }
  .herf {
    text-decoration: underline;
  }
}
</style>
