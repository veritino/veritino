<script lang="ts">
import headerImage from '../assets/images/veritino/veritino-banner.png'
</script>

<header>
  <div class="navbar">
    <div class="navbar_left">
      <img src={headerImage} alt="aaa">
    </div>
    <div class="navbar_right">
      <a href="/">ホーム</a>
      <a href="/">メンバー</a>
      <a href="/">プロジェクト</a>
    </div>
  </div>
</header>

<style lang="scss" scoped>
:root {
  --axuata-normal-fontcolor-header: #0B0B0F;
  --axuata-normal-fontcolor-tag: #5c5c5c;
  --axuata-normal-fontcolor-description: #424242;
}
 
header {
  top: 0;
  position: sticky;
  background-color: #ffffff;

  .navbar {
    justify-content: space-between;
    height: 64px;
    align-items: center;
    display: flex;

    .navbar_left {
      img {
        height: 50px;
      }
    }

    .navbar_right {
      a {
        font-size: 16px;
        font-weight: 700;
        color: var(--axuata-normal-fontcolor-header);
        text-decoration: none;
        margin-right: 10px;
      }
    }
  }
}
</style>