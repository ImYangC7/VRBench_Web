<script>
export default {
  data() {
    return {
      bibtex: [
        '@article{junyaohu2023template,',
        '    title={Academic Project Page Template Vue},',
        '    author={Hu, Junyao},',
        '    journal={GitHub},',
        '    year={2023}',
        '}',
      ],
    }
  },
  methods: {
    copyVal() {
      const oInput = document.createElement('textarea')
      const text = document.getElementById('bibtex')?.innerText || ''
      oInput.value = text
      document.body.appendChild(oInput)
      oInput.select()
      document.execCommand('Copy')
      this.$message.success('Copy Successfully')
      oInput.remove()
    },
  },
}
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">BibTeX</h1>
    </el-row>

    <el-row justify="center">
      <el-col
        class="bibtex"
        :xs="24"
        :sm="20"
        :md="14"
        :lg="12"
        :xl="12"
        @click="copyVal()"
      >
        <div class="bibtex-note">
          Please consider citing our paper if our work is useful.
        </div>
        <div class="bibtex-hint">
          🖱️ Click here to copy BibTex.
        </div>
        <el-row>
          <el-scrollbar style="margin: 0 20px 5px 20px">
            <pre id="bibtex">
<code v-for="b in bibtex" :key="b">{{ b }}<br/></code>
            </pre>
          </el-scrollbar>
        </el-row>
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
.scrollbar-flex-content {
  display: flex;
}

.bibtex {
  margin: 20px 0;
  padding-top: 5px;
  box-shadow: var(--el-box-shadow-light);
  border-radius: 10px;
}

.bibtex:hover {
  box-shadow: var(--el-box-shadow);
}

.bibtex:active {
  box-shadow: var(--el-box-shadow-lighter);
}

.bibtex-note {
  text-align: center;
  color: var(--el-text-color-secondary);
  margin-top: 16px;
}

.bibtex-hint {
  text-align: center;
  color: var(--el-text-color-secondary);
  margin-top: 4px;
}

pre {
  border: none;
  border-radius: 0;
  padding: 10px;
  background: none;
}

pre code {
  font-size: 18px;
  background: #ffffff;
}
</style>
