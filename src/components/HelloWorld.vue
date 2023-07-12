<template>
  <v-container>
    <v-row>
      <template v-for="(project, i) in projects" :key="i">
        <v-col cols="4">
          <v-card class="mx-auto" max-width="344">
            <v-img
              :src="project.img"
              height="200px"
              cover
            ></v-img>

            <v-card-title> {{ project.name }}</v-card-title>

            <v-card-subtitle> {{ project.description }}</v-card-subtitle>

            <v-card-actions>
              <a :href="project.link" target="_blank">
                <v-btn color="orange-lighten-2" variant="text"> Explore</v-btn>
              </a>
            </v-card-actions>
          </v-card>
        </v-col>
      </template>

    </v-row>
  </v-container>
</template>

<script lang="ts" setup>
// 项目汇总
const projects = [
  {
    "name": "多巴胺随机歌词",
    "img": "/images/random_quote_song_lrcs.gif",
    "description": "从存档的lrc文件中, 随机选取歌词进行展示",
    "link": "https://github.com/HongXiaoHong/front_road/tree/random-quote-machine",
    "api_project": {
      "link": "https://github.com/HongXiaoHong/applets/tree/random-quote-machine",
      "language": "python"
    }
  },
  {
    "name": "冰火两仪眼-太极-音乐磁场-解析器",
    "img": "/images/music_magnetic_field_analyzer.gif",
    "description": "爬取音乐磁场, 下载到本地",
    "link": "https://github.com/HongXiaoHong/front_road/tree/music_magnetic_field_analyzer",
    "api_project": {
      "link": "https://github.com/HongXiaoHong/applets/tree/music_magnetic_field_analyzer",
      "language": "python"
    }
  },
  {
    "name": "平平无奇 markdown 编辑器",
    "img": "/images/simple_markdown_previewer.gif",
    "description": "实时编译 markdown 内容",
    "link": "https://github.com/HongXiaoHong/front_road/tree/simple_markdown_previewer",
    "api_project": {
      "link": "",
      "language": ""
    }
  },
];
</script>
