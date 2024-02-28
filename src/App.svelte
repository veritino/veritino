<script lang="ts">
import VeritinoHeader from "./lib/VeritinoHeader.svelte";
import VeritinoWelcome from "./lib/VeritinoWelcome.svelte";
import VeritinoSection from "./lib/VeritinoSection.svelte";
import VeritinoCard from "./lib/VeritinoCard.svelte";
import VeritinoFooter from "./lib/VeritinoFooter.svelte";

import cardProjectImageVeritino from './assets/images/veritino/veritino.png'
import cardMemberImageAxuata from "./assets/images/_members/axuata.png";
import cardMemberImageRetrip from "./assets/images/_members/retrip.png";
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
    <VeritinoCard imagePath={cardMemberImageRetrip} cardTitle="Retrip" cardDescription="
      <p>Veritinoのメンバー</p>
      <a href='https://github.com/samayoeru-pita'>Github</a>
    "/>
  </VeritinoSection>
  <VeritinoSection sectionTitle="プロジェクト" sectionDescription="
    <p>Veritinoのプロジェクトリストです。</p>
  ">
    <VeritinoCard imagePath={cardProjectImageVeritino} cardTitle="Veritino" cardDescription="
      <p>Veritinoのウェブサイト</p>
      <a href='https://github.com/veritino/veritino'>Github</a>
    "/>
    <VeritinoCard imagePath={cardProjectImageVeritino} cardTitle="Veritibot" cardDescription="
      <p>VeritinoのDiscordサーバー用に作られたBOT</p>
      <a href='https://github.com/veritino/veritibot'>Github</a>
    "/>
  </VeritinoSection>
  <VeritinoFooter />
</main>

<style>
  
</style>
