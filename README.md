- 👋 Hello, I'm Alishangtian from 360
- 🌐 Interests: AIGC and AGI.
- 🧠 Expertise: Deeply involved in LLMs, Agent, MultiAgent, SFT, RL, RLHF, Agentic-Workflow.
- 🤝 Collaboration: Open to collaborating on any projects or ideas.
- 📧 Contact: You can reach me at alishangtian@gmail.com.
<!---
alishangtian/alishangtian is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
# 探索AI与技术的未来

## 🌟 About Me

你好！我是来自360的 **Alishangtian**，一位致力于推动AI技术边界的研究者和实践者。

> "The future belongs to those who believe in the beauty of their dreams."

<div class="github-stats">
<script>
// GitHub统计
fetch('https://api.github.com/users/alishangtian')
  .then(response => response.json())
  .then(data => {
    document.getElementById('github-followers').textContent = data.followers;
    document.getElementById('github-repos').textContent = data.public_repos;
    document.getElementById('github-stars').textContent = data.public_gists;
  })
  .catch(error => {
    console.error('Error fetching GitHub stats:', error);
    document.querySelector('.stats-container').innerHTML = '<p>GitHub统计加载中...</p>';
  });

// arXiv最新AI论文
fetch('https://export.arxiv.org/api/query?search_query=cat:cs.AI+OR+cat:cs.LG&sortBy=lastUpdatedDate&sortOrder=descending&max_results=3')
  .then(response => response.text())
  .then(str => new window.DOMParser().parseFromString(str, "text/xml"))
  .then(data => {
    const entries = data.getElementsByTagName('entry');
    let html = '<ul>';
    for (let i = 0; i < entries.length; i++) {
      const title = entries[i].getElementsByTagName('title')[0].textContent;
      const link = entries[i].getElementsByTagName('id')[0].textContent;
      html += `<li><a href="${link}" target="_blank">${title}</a></li>`;
    }
    html += '</ul>';
    document.getElementById('arxiv-papers').innerHTML = html;
  })
  .catch(error => {
    console.error('Error fetching arXiv papers:', error);
    document.getElementById('arxiv-papers').innerHTML = '<p>论文加载中...</p>';
  });

// Papers with Code热门项目
fetch('https://paperswithcode.com/api/v1/papers/?ordering=-twitter_mentions')
  .then(response => response.json())
  .then(data => {
    let html = '<ul>';
    data.results.slice(0, 3).forEach(paper => {
      html += `<li><a href="${paper.url}" target="_blank">${paper.title}</a></li>`;
    });
    html += '</ul>';
    document.getElementById('trending-papers').innerHTML = html;
  })
  .catch(error => {
    console.error('Error fetching trending papers:', error);
    document.getElementById('trending-papers').innerHTML = '<p>热门项目加载中...</p>';
  });
</script>

<div class="stats-container">
<p>GitHub统计：</p>
<p>👥 关注者：<span id="github-followers">Loading...</span></p>
<p>📚 公开仓库：<span id="github-repos">Loading...</span></p>
<p>⭐ Stars：<span id="github-stars">Loading...</span></p>
</div>
</div>

## 🔮 Research Focus

- **AIGC & AGI**: 探索通用人工智能的无限可能
- **Large Language Models**: 深度参与LLMs的研究与应用
- **Agent & MultiAgent**: 构建智能体系统，探索多智能体协作
- **Reinforcement Learning**: 专注于SFT、RL、RLHF等前沿技术
- **Agentic-Workflow**: 打造下一代智能工作流程

## 💡 Vision

在这个AI快速发展的时代，我们正站在技术革新的浪潮之巅。通过这个博客，我希望能与您分享：

- 前沿技术的深度洞察
- AI研究的最新进展
- 实践中的经验与思考
- 对技术未来的展望

<div class="dynamic-content">
<div class="papers-container">
  <div class="arxiv-box">
    <h3>📄 最新AI研究论文</h3>
    <div id="arxiv-papers">Loading papers...</div>
  </div>
  
  <div class="trending-box">
    <h3>🔥 热门AI项目</h3>
    <div id="trending-papers">Loading trending papers...</div>
  </div>
</div>

<script>
// 每日技术名言
fetch('https://api.quotable.io/random?tags=technology,science')
  .then(response => response.json())
  .then(data => {
    document.getElementById('daily-quote').textContent = `"${data.content}"`;
    document.getElementById('quote-author').textContent = `- ${data.author}`;
  })
  .catch(error => {
    console.error('Error fetching quote:', error);
    document.querySelector('.quote-box').innerHTML = '<p>每日名言加载中...</p>';
  });
</script>

<div class="quote-box">
<p>今日技术名言：</p>
<p id="daily-quote">Loading quote...</p>
<p id="quote-author"></p>
</div>
</div>

## 🤝 Connect

期待与您一起探讨技术，分享创新：

- 📧 Email: alishangtian@gmail.com
- 🔗 GitHub: [alishangtian](https://github.com/alishangtian)
- 💬 欢迎通过评论或Issue交流

<style>
.stats-container, .quote-box, .arxiv-box, .trending-box {
    background: rgba(255, 255, 255, 0.1);
    padding: 20px;
    border-radius: 10px;
    backdrop-filter: blur(10px);
    margin: 20px 0;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
}

.stats-container:hover, .quote-box:hover, .arxiv-box:hover, .trending-box:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 8px rgba(0, 0, 0, 0.15);
}

.papers-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin: 20px 0;
}

.dynamic-content {
    margin: 40px 0;
}

#daily-quote {
    font-style: italic;
    font-size: 1.1em;
    color: #2196F3;
    line-height: 1.6;
}

#quote-author {
    text-align: right;
    color: #666;
    margin-top: 10px;
}

.github-stats p {
    margin: 10px 0;
    font-size: 1.1em;
}

.github-stats span {
    color: #2196F3;
    font-weight: bold;
}

.arxiv-box h3, .trending-box h3 {
    color: #2196F3;
    margin-bottom: 15px;
}

.arxiv-box ul, .trending-box ul {
    list-style: none;
    padding: 0;
}

.arxiv-box li, .trending-box li {
    margin: 10px 0;
    padding: 10px;
    background: rgba(255, 255, 255, 0.05);
    border-radius: 5px;
    transition: all 0.2s ease;
}

.arxiv-box li:hover, .trending-box li:hover {
    background: rgba(255, 255, 255, 0.1);
}

.arxiv-box a, .trending-box a {
    color: #666;
    text-decoration: none;
    display: block;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}

.arxiv-box a:hover, .trending-box a:hover {
    color: #2196F3;
}

@media (max-width: 768px) {
    .papers-container {
        grid-template-columns: 1fr;
    }
}
</style>

---

> "The best way to predict the future is to invent it."
>
> -- Alan Kay
