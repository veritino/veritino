<script lang="ts">
const repoOwner: string = 'veritino';
const repoName: string = 'veritino';
const apiUrl: string = `https://api.github.com/repos/${repoOwner}/${repoName}/commits`;

fetch(apiUrl)
  .then((response: Response) => {
    if (!response.ok) {
      throw new Error('WARN: ネットワークのレスポンスが悪いです。');
    }
    return response.json();
  })
  .then((data: any[]) => {
    const latestCommitMessage: string = data[0].commit.message;
    const latestCommitUrl: string = data[0].html_url;
    const latestCommitId: string = data[0].sha.slice(0, 7);
    setLatestCommitElement(latestCommitUrl, latestCommitId);
  })
  .catch((error: Error) => {
    console.error('WARN: フェッチ操作に問題がありました：', error);
  });

function setLatestCommitElement(commitUrl: string, commitId: string): void {
  let latestCommitElement: HTMLElement | null = document.getElementById('latestCommit');
  if (latestCommitElement) {
    let latestCommitAnchor: HTMLAnchorElement | null = latestCommitElement.querySelector('a');
    if (latestCommitAnchor) {
      latestCommitAnchor.href = commitUrl;
      latestCommitAnchor.textContent = commitId;
      console.log(`latestCommitAnchorのhrefが ${commitUrl} に設定されました`);
      console.log(`latestCommitAnchorのtextContentが ${commitId} に設定されました`);
    } else {
      console.error('WARN: latestCommitのアンカーが見つかりませんでした。');
    }
  } else {
    console.error('WARN: latestCommitが見つかりませんでした。');
  }
}

</script>

<footer>
  <p id="latestCommit">最終更新：<a href="">CommitLink</a></p>
  <p>© 2024 - 2024 Veritino - All Rights Reserved</p>
</footer>

<style lang="scss" scoped>
footer {
  padding: 20px;

  p {
    text-align: center;
  }
}
</style>