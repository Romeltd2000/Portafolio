<template>
  <div class="about">
    <j-baner :text="'Sobre Mi'"/>
    <div class="content-about">
      <div class="info-me w-50">
        <div v-for="info in infoMe" :key="info.title">
          <h2>{{ info.title }}</h2>
          <p>{{ info.content }}</p>
        </div>
      </div>
      <div class="skills-me w-50">
        <div class="skills" v-for="skill in skillsMe" :key="skill.title">
          <v-img class="skills-img" :lazy-src="skill.icon" :src="skill.icon" alt="icon" max-width="80" max-height="80" ></v-img>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import JBaner from '@/utils/JBaner.vue'
export default {
  components: { JBaner },
  name: 'AboutView',
  data () {
    return {
      infoMe: [
        {
          title: 'Estudios',
          content: 'Soy estudiante universitario de la carrera de Ingeniería de Sistemas e Informática, con una sólida formación técnica en diseño gráfico especializado en Adobe Illustrator y Photoshop. He complementado mis estudios con diplomados en Gestión de Importación Internacional y Logística, así como en Excel Profesional, Data Analyst en Macros VBA, y Power BI, lo que me ha permitido desarrollar habilidades multidisciplinarias en tecnología, diseño y gestión.'
        },
        {
          title: 'Experiencia',
          content: 'Mi experiencia profesional se ha centrado en roles técnicos y de calidad dentro de la industria tecnológica y de entretenimiento. He trabajado como Operador de Equipos de Juego Electrónico, donde adquirí conocimiento en la operación y mantenimiento de sistemas de juegos, asegurando su funcionamiento óptimo. Además, me desempeñé como Gestor de Garantía de Calidad de Software y Aplicaciones, donde fui responsable de supervisar y mejorar la calidad del software, asegurando que las aplicaciones cumplieran con los estándares más altos de rendimiento y usabilidad. Estas experiencias me han brindado una sólida base en operaciones técnicas y control de calidad, fundamentales para el desarrollo de soluciones eficientes y confiables.'
        },
        {
          title: 'Propósito',
          content: 'Mi propósito como estudiante de Ingeniería de Sistemas e Informática es desarrollar soluciones tecnológicas innovadoras que optimicen procesos y mejoren la eficiencia en diversas áreas. Me apasiona el aprendizaje continuo y la aplicación de nuevas tecnologías para crear un impacto positivo en la sociedad. Busco crecer profesionalmente en un entorno dinámico, donde pueda aportar mis conocimientos y habilidades mientras sigo ampliando mis competencias.'
        }
      ],
      skillsMe: [
        {
          icon: 'https://cdn-icons-png.flaticon.com/512/5968/5968267.png',
          title: 'HTML'
        },
        /*
        {
          icon: 'https://cdn-icons-png.flaticon.com/512/5968/5968242.png',
          title: 'CSS'
        },
        */
        {
          icon: 'https://cdn-icons-png.flaticon.com/512/5968/5968292.png',
          title: 'JavaScript'
        },
        /*
        {
          icon: 'https://upload.wikimedia.org/wikipedia/commons/thumb/b/b2/Bootstrap_logo.svg/800px-Bootstrap_logo.svg.png',
          title: 'Boostrap'
        },
        {
          icon: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/250px-Vue.js_Logo_2.svg.png',
          title: 'Vue'
        },
        {
          icon: 'https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Node.js_logo.svg/1200px-Node.js_logo.svg.png',
          title: 'Node'
        },
        */
        {
          icon: 'https://cdn-icons-png.flaticon.com/512/5968/5968332.png',
          title: 'PHP'
        },
        {
          icon: 'https://docs.nestjs.com/assets/logo-small.svg',
          title: 'NestJS'
        },
        /*
        {
          icon: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Laravel.svg/1200px-Laravel.svg.png',
          title: 'Laravel'
        },
        */
        {
          icon: 'https://d1.awsstatic.com/asset-repository/products/amazon-rds/1024px-MySQL.ff87215b43fd7292af172e2a5d9b844217262571.png',
          title: 'MySQL'
        },
        {
          icon: 'https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Postgresql_elephant.svg/640px-Postgresql_elephant.svg.png',
          title: 'PostgresSQL'
        },
        {
          icon: 'https://miro.medium.com/max/512/1*doAg1_fMQKWFoub-6gwUiQ.png',
          title: 'MongoDB'
        },
        /*
        {
          icon: 'https://upload.wikimedia.org/wikipedia/commons/thumb/1/17/GraphQL_Logo.svg/800px-GraphQL_Logo.svg.png',
          title: 'GraphQL'
        },
        */
        {
          icon: 'https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/1200px-Python-logo-notext.svg.png',
          title: 'Python'
        },
        {
          icon: 'https://cdn.icon-icons.com/icons2/2107/PNG/512/file_type_flutter_icon_130599.png',
          title: 'Flutter'
        }
      ]
    }
  }
}
</script>

<style scoped>
.about{
  height: 80vh;
}
.content-about{
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 2% 10%;
}
.w-50{
  width: 50%;
  margin: 1%;
}

.info-me h2{
  color: #fff;
}

.info-me p{
  color: rgba(255, 255, 255, 0.582);
}

.skills-me{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  justify-content: center;
  align-items: center;
  background-color: hsla(0, 0%, 100%, 0.527);
  border-radius: 15px;
  box-shadow: 10px 15px 1px rgba(255, 255, 255, 0.329);
}

.skills .skills-img{
  margin: 15px 20px;
}

</style>
