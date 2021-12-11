<template>
  <div class="bg-gray-100 p-4 rounded">
    <div class="font-bold text-green-600 text-2xl">Information</div>
    <div v-for="item in lists" :key="item.name" class="my-2">
        <div class="text-lg text-blue-500 ml-3">- {{item.name}}</div>
        <div v-for="line in item.data" :key="line.title" class="my-2">
            {{line.title}}: {{line.message}}
        </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
        lists: [
        {
          name: "Basic",
          data: [
            {
              title: "Birthday",
              message: "14/04",
            },
            {
              title: "Gender",
              message: "Male",
            },
            {
              title: "E-mail",
              message: "no1.ily1606@gmail.com",
            },
            {
              title: "Slogan",
              message:
                "Losing isn't fun. That's why I don't do it. - Pathfinder (Apex Lengends)",
            },
            {
              title: "Hobby",
              message: "Coding, music, game",
            },
          ],
        },
        {
          name: "Job",
          data: [
            {
              title: "Learning",
              message:
                "K19 - VKU (VietNam - Korea University of information and communication technology)",
            },
            {
              title: "Job",
              message: "Programer",
            },
            {
              title: "Working",
              message: "Pracelsoft Da Nang",
            },
          ],
        },
        {
          name: "Knowledge",
          data: [
            {
              title: "Languages",
              message: "Javascript, PHP, Python, Java",
            },{
              title: "Databases",
              message: "Maria database, SQL Server, Redis",
            },{
              title: "DevOPS",
              message: "Docker, Apache, Ubuntu, Windows server, IIS",
            },{
              title: "Frameworks",
              message: "Frameworks: VueJS (Vue 2, Vue 3), NuxtJS, Jquery, Laravel, Bootstrap 4, TailwindCSS",
            },{
              title: "Other techniques",
              message: "Chrome extension, python adb (for automatic), npm, git (github, gitlab), sass, PWA",
            },{
              title: "Application security",
              message: "Basic (XSS, SQL Injection, JWT,...)",
            },
          ],
        },
      ],
    };
  },
};
</script>
