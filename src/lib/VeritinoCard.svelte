<script lang="ts">
export let imagePath: string;
export let cardTitle: string;
export let cardDescription: string;
</script>

<div class="card">
  <div class="card_left">
    <img src={imagePath} alt="">
  </div>
  <div class="card_right">
    <p class="card_title">{cardTitle}</p>
    <p class="card_description">{@html cardDescription}</p>
  </div>
</div>

<style lang="scss" scoped>
:root {
  --axuata-normal-fontcolor-header: #0B0B0F;
  --axuata-normal-fontcolor-tag: #5c5c5c;
  --axuata-normal-fontcolor-description: #424242;
}

.card {
  display: flex;
  align-items: center;

  .card_left {
    padding: 12px 0;

    img {
      border-radius: 32px;
      height: 100px;
    }
  }

  .card_right {
    margin-left: 20px;
    align-items: center;
    
    .card_title {
      line-height: 120%;
      font-weight: 700;
      font-size: 28px;
    }

    .card_description {
      line-height: 130%;
      color: var(--axuata-normal-fontcolor-description);
      font-weight: 700;
    }
  }
}
</style>