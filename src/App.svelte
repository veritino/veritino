<script lang="ts">
import VeritinoHeader from "./lib/VeritinoHeader.svelte";
import VeritinoWelcome from "./lib/VeritinoWelcome.svelte";
import VeritinoSection from "./lib/VeritinoSection.svelte";
</script>

<main>
  <VeritinoHeader />
  <VeritinoWelcome />
  <VeritinoSection sectionTitle="ようこそ" sectionDescription="
    <p>Veritinoは新しい開発チームです。 </p>
    <p>技術を練習し実践するためにこの組織を設立しました。</p>
    <p><a href='https://github.com/veritino'>Github</a> / <a href='https://discord.gg/UY9Nx4Dnvg'>Discordサーバー</a></p>
  "></VeritinoSection>
  <VeritinoSection sectionTitle="メンバー" sectionDescription="
    <p>Veritinoのメンバーリストです。</p>
  ">
  <p>作り途中</p>
  </VeritinoSection>
</main>

<style>
  
</style>
