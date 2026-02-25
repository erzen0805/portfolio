<script>
  import ImageBox from './ImageBox.svelte';
</script>

<h3 class="subtitle">프로토콜</h3>
<ImageBox source="img/skill/tcp.png" title="TCP/IP" />
<ImageBox source="img/skill/http.png" title="HTTP" />
<ImageBox source="img/skill/modbus.png" title="MODBUS" />
<ImageBox source="img/skill/iec61850.png" title="IEC61850" />

<h3 class="subtitle">데이터베이스</h3>
<ImageBox source="img/skill/mssql.png" title="MSSQL" />
<ImageBox source="img/skill/mysql.png" title="MySQL" />
<ImageBox source="img/skill/oracle.png" title="OracleDB" />
<ImageBox source="img/skill/sqlite.png" title="SQLite" />
<ImageBox source="img/skill/redis.png" title="Redis" />

<h3 class="subtitle">협업 / 버전관리</h3>
<ImageBox source="img/skill/git.png" title="Git" />
<ImageBox source="img/skill/svn.png" title="SVN" />
<ImageBox source="img/skill/jira.png" title="Jira" />
<ImageBox source="img/skill/redmine.png" title="Redmine" />
<ImageBox source="img/skill/notion.png" title="Notion" />

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
