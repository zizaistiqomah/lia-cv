<template>
  <div class="container">
    <div class="row mt-5">
      <div class="col-md-4 text-center">
        <h3 class="mt-3">{{ profile.name }}</h3>
        <p>{{ profile.title }}</p>
      </div>
      <div class="col-md-8 ">
        <h4>About Me</h4>
        <p>{{ profile.about }}</p>

        <h4>Skills</h4>
        <ul>
          <li v-for="skill in profile.skills" :key="skill">{{ skill }}</li>
        </ul>

        <h4>Experience</h4>
        <ul>
          <li v-for="experience in profile.experience" :key="experience.company">
            <strong>{{ experience.company }}</strong> - {{ experience.role }} ({{ experience.period }})
            <p>{{ experience.description }}</p>
          </li>
        </ul>

        <h4>Education</h4>
        <ul>
          <li v-for="education in profile.education" :key="education.school">
            <strong>{{ education.school }}</strong> - {{ education.degree }} ({{ education.period }})
            <p>{{ education.description }}</p>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      profile: {
        name: 'AMANDA AURELIA',
        title: 'Graphic Designer',
        about: 'Saya adalah seorang desainer grafis yang berpengalaman dan berkecimpung di industri kreatif. Saya memiliki keahlian dalam membuat desain visual yang menarik dan fungsional, mulai dari branding, desain web, hingga media sosial. Dengan kombinasi kreativitas, detail, dan pemahaman yang mendalam tentang prinsip-prinsip desain, saya selalu berusaha menghadirkan solusi visual yang sesuai dengan kebutuhan klien. Pengalaman saya mencakup kolaborasi dengan berbagai perusahaan serta bekerja secara freelance untuk klien internasional.',
        skills: ['Adobe Photoshop', 'Illustrator', 'InDesign', 'Branding', 'UI/UX Design'],
        experience: [
          {
            company: 'Studio Kreatif XYZ',
            role: 'Lead Graphic Designer',
            period: '2020 - Present',
            description: 'Bertanggung jawab atas seluruh proses desain dari konsep hingga finalisasi, memastikan kualitas desain sesuai standar.'
          },
          {
            company: 'Freelance',
            role: 'Graphic Designer',
            period: '2020 - present',
            description: 'Mengerjakan berbagai proyek desain untuk klien lokal dan internasional, termasuk branding, media sosial, dan materi promosi.'
          }
        ],
        education: [
          {
            school: 'SMKN 12 MALANG',
            degree: 'Bachelor of Arts in Graphic Design',
            period: '2020 - present',
            description: 'Fokus pada desain visual, tipografi, dan komunikasi visual.'
          }
        ]
      }
    }
  }
}
</script>

<style>
.container {
  max-width: 900px;
  margin: 0 auto;
}
</style>

