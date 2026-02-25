<script>
  import ImageBox from './ImageBox.svelte';
</script>

<h3 class="subtitle">데스크톱</h3>
<ImageBox source="img/skill/mfc.png" title="MFC" />
<ImageBox source="img/skill/qt.png" title="Qt C++" />
<ImageBox source="img/skill/winform.png" title=".NET WinForm" />
<ImageBox source="img/skill/wpf.png" title=".NET WPF" />
<ImageBox source="img/skill/lightning_chart.png" title="LightningChart" />

<h3 class="subtitle">서버 / 백엔드</h3>
<ImageBox source="img/skill/dotnetcore.png" title=".NET Core" />
<ImageBox source="img/skill/java.png" title="Java" />
<ImageBox source="img/skill/java_spring.png" title="Java Spring" />
<ImageBox source="img/skill/kotlin.png" title="Kotlin" />
<ImageBox source="img/skill/go.png" title="GO" />

<h3 class="subtitle">AI / 데이터</h3>
<ImageBox source="img/skill/python.png" title="Python" />
<ImageBox source="img/skill/jupyter_notebook.png" title="Jupyter Notebook" />
<ImageBox source="img/skill/keras.png" title="Keras" />

<style>
.subtitle {
  grid-column: 1 / -1;
  color: rgb(200, 200, 200);
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  margin: 16px 0 4px 0;
  padding-bottom: 4px;
  border-bottom: 1px solid rgb(100, 100, 100);
}
.subtitle:first-child {
  margin-top: 4px;
}
</style>
