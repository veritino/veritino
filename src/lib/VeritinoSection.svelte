<script lang="ts">
export let sectionTitle: string;
export let sectionDescription: string;
</script>

<div class="section">
  <p class="section-title">{sectionTitle}</p>
  <p class="section-description">{@html sectionDescription}</p>
  <slot></slot>
</div>

<style lang="scss" scoped>
:root {
  --axuata-normal-fontcolor-header: #0B0B0F;
  --axuata-normal-fontcolor-tag: #5c5c5c;
  --axuata-normal-fontcolor-description: #424242;
}

.section {
  margin: 56px 10px;
  .section-title {
    font-size: 34px;
    font-weight: 700;
  }

  .section-title::before {
    color: var(--axuata-normal-fontcolor-tag);
    margin-right: 4px;
    content: '#';
  }

  .section-description {
    color: var(--axuata-normal-fontcolor-description);
    font-weight: 700;
  }
}
</style>