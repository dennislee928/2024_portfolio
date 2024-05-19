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
          </div>
        </div>
        <div class="center-side">
          <div class="nft-section">
            <div class="nft-text">
              <!-- NFT Text -->
              <p class="nft-info-text">
                First student to create dynamic
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
  width: 100vw;
  height: 100vh;
}

.left-side,
.project2-3 {
  margin: 5px;
}

.project1-image,
.project1-text,
.easte-egg {
  margin: 5px;
}

.title {
  font-size: max(2vw, 18px);
  margin: 5px;
}

.projects-container,
.left-side,
.center-side,
.right-side {
  display: flex;
  flex-direction: column;
  margin: 5px;
}

.project-image,
.project-text,
.nft-section,
.nft-image,
.nft-text,
.meta-image,
.meta-text,
.edu-image,
.edu-text {
  margin: 5px;
}

/* 調整所有包含圖片的 div，使其長寬保持 1:1 並裁剪圖片 */
.project1-image,
.project-image,
.nft-image,
.meta-image,
.edu-image {
  width: 100%; /* 或設定為特定寬度，例如 width: 25vw; */
  height: 0; /* 初始設為 0 */
  padding-top: 100%; /* 高度等於自身寬度，形成正方形 */
  position: relative; /* 定位相對於包含元素 */
}

.project1-image img,
.project-image img,
.nft-image img,
.meta-image img,
.edu-image img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover; /* 裁剪並填滿 div 而不失真 */
}

/* 手機裝置的 CSS 媒體查詢 */
@media (max-width: 768px) {
  .left-side {
    width: 30%;
  }
  .project2-3 {
    flex-direction: column;
    width: 100%;
  }
  .center-side {
    width: 30%;
  }
  .right-side {
    width: 30%;
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
    width: 115%;
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
