<script lang="ts">
import VeritinoHeader from "./lib/VeritinoHeader.svelte";
import VeritinoWelcome from "./lib/VeritinoWelcome.svelte";
import VeritinoSection from "./lib/VeritinoSection.svelte";
import VeritinoCard from "./lib/VeritinoCard.svelte";
import VeritinoFooter from "./lib/VeritinoFooter.svelte";

import cardProjectImageVeritino from './assets/images/veritino/veritino.png'
import cardMemberImageAxuata from "./assets/images/_members/axuata-wb.png";
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
    <VeritinoCard imagePath={cardMemberImageAxuata} cardTitle="Axuata" cardDescription="
      <p>Veritinoの管理者</p>
      <a href='https://github.com/axuata'>Github</a>
    "/>
  </VeritinoSection>
  <VeritinoSection sectionTitle="プロジェクト" sectionDescription="
    <p>Veritinoのプロジェクトリストです。</p>
  ">
    <VeritinoCard imagePath={cardProjectImageVeritino} cardTitle="Axuata" cardDescription="
      <p>Veritinoのウェブサイト</p>
      <a href='https://github.com/veritino/veritino'>Github</a>
    "/>
  </VeritinoSection>
  <VeritinoFooter />
</main>

<style>
  
</style>
