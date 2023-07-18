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

            <v-divider class="mx-4"></v-divider>

            <v-card-text class="d-flex flex-wrap">
              <v-chip v-for="skill in project.skills">
                {{ skill }}
              </v-chip>
            </v-card-text>

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
    "skills": ["html", "css", "javascript", "jquery"],
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
    "skills": ["html", "css", "javascript", "sweetalert2", "jquery"],
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
    "skills": ["react",
      "babel",
      "webpack",
      "webpack-loader",
      "marked",
      "highlight",
    ],
    "api_project": {
      "link": "",
      "language": ""
    }
  },
  {
    "name": "早睡身体好播放器",
    "img": "/images/early_bed_healthy_player.gif",
    "description": "获取本地歌单播放",
    "link": "https://github.com/HongXiaoHong/front_road/tree/early_bed_healthy_player",
    "skills": ["html", "css", "javascript", "font-awesome", "particles", "jquery"],
    "api_project": {
      "link": "https://github.com/HongXiaoHong/applets/tree/early_bed_healthy_player",
      "language": "python"
    }
  },
  {
    "name": "小学生都不用计算器",
    "img": "/images/elementary_school_students_calculator.gif",
    "description": "小学生加减乘除",
    "link": "https://github.com/HongXiaoHong/front_road/tree/elementary_school_students_calculator",
    "skills": ["html", "css", "javascript", "bootstrap", "jquery"],
    "api_project": {
      "link": "",
      "language": ""
    }
  },
  {
    "name": "美国 GDP 展示",
    "img": "/images/d3.gif",
    "description": "美国 GDP 柱状图",
    "link": "https://github.com/HongXiaoHong/front_road/tree/d3",
    "skills": ["html", "css", "javascript", "es6", "d3"],
    "api_project": {
      "link": "",
      "language": ""
    }
  },
];

</script>
